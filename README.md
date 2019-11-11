# missing-lint-check-for-observe
This repo is created to showcase missing lint check, when using observe extension method in a Fragment.

When running lint task on TestFragment with `androidx.fragment:fragment-ktx:1.2.0-rc02`
the `FragmentLiveDataObserve` lint check doesn't report errors for `liveData.observe(this) {}` or `liveData.observe(this, {})`.
Only error is reported for `liveData.observe(this, Observer {  })`.
