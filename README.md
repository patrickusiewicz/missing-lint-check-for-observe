# missing-lint-check-for-observe

`androidx.fragment:fragment-ktx:1.2.0-rc02` library contains lint checks for when one doesn't use `viewLifecycleOwner` property as LifecycleOwner, while observing LiveData in a Fragment. This repository shows the added lint check is missing a check for when one uses the `observe` extension function instead of the class function.

When running lint task on the project the `FragmentLiveDataObserve` lint check doesn't report errors for `liveData.observe(this) {}` or `liveData.observe(this, {})`, which are extension functions.
Only error is reported for `liveData.observe(this, Observer {  })`.
