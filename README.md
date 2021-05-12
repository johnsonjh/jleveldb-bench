# jleveldb-bench

`jleveldb-bench` tests `jleveldb` performance.

## Installation

* `go install -v ./...`

## Operation

* Run with `ldb-writebench`:

  * `mkdir datasets/mymachine-10gb`
  * `ldb-writebench -size 10gb -logdir datasets/mymachine-10gb -test nobatch,batch-100kb`

* Plot the result with `ldb-benchplot`:

  * `ldb-benchplot -out 10gb.svg datasets/mymachine-10gb/*.json`

* Databases are left on disk for inspection. You can remove them using:

  * `rm -r jtestdb-*`
