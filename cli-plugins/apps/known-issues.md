# Known Issues

* `--image`:
  - This flag isn't supported by the supply chain in Tanzu Application Platform Beta 2 release.
* `tanzu apps workload get`:
  - passing in `--output json` along with and the `--export` flag will return yaml rather than json (support for honoring the `--output json` in conjunction with `--export` will be added in the next release).
* `tanzu apps workload create/update/apply`:
   - `--wait` functions as expected when a workload is created for the first time but may return prematurely on subsequent updates (when passed in with `workload update/apply` for existing workloads). 
   - when the `--wait` flag has been included and the "Do you want to create this workload?" prompt is declined, the command continues to wait rather exit.