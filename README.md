# NeoMutt Fuzzing

This repo contains the 'corpus' of test cases for testing two NeoMutt library
functions:

- `mutt_rfc822_read_header()`
- `mutt_parse_part()`

These are used by OSS-Fuzz, an automated fuzzing tool.
While running it will also generate more test cases.

## OSS-Fuzz

- Continuous Fuzzing ([README](https://github.com/google/oss-fuzz/))
- [Test case data](corpus)
- Test harness: [test-fuzz](https://github.com/neomutt/test-library)

## Private Area

For security, the bug reports that OSS-Fuzz generates aren't available to the
public.

- [List of open bugs](https://bugs.chromium.org/p/oss-fuzz/issues/list?q=label:Proj-neomutt)
- [OSS-Fuzz overview of Fuzzers](https://oss-fuzz.com/)
- Google Cloud Storage [bucket containing test cases](https://console.cloud.google.com/storage/browser/neomutt-corpus.clusterfuzz-external.appspot.com/libFuzzer/neomutt_address-fuzz/?pli=1)

The latest corpus can be downloaded using `gsutil`

- [Download gsutil](https://cloud.google.com/storage/docs/gsutil_install)
- Download test cases:
  `gsutil -m rsync gs://neomutt-corpus.clusterfuzz-external.appspot.com/libFuzzer/neomutt_address-fuzz corpus/`

