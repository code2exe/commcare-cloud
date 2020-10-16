<!--THIS FILE IS AUTOGENERATED: DO NOT EDIT-->
<!--See https://github.com/dimagi/commcare-cloud/blob/master/changelog/README.md for instructions-->
# 37. Run command to update Supervisor configurations

**Date:** 2020-10-14

**Optional per env:** _required on all environments_


## CommCare Version Dependency
The following version of CommCare must be deployed before rolling out this change:
[05ebc51b](https://github.com/dimagi/commcare-hq/commit/05ebc51ba4b16a420f0fd64c17ffad89501ea36d)


## Change Context
Run management command to remove unused errand-boy processes.

## Details
The `errand-boy` package is no longer required. It's corresponding process
group should be removed to avoid deploy errors when restarting services
when `errand-boy` is not installed.

## Steps to update
Run the following management command to update supervisor configs:

```bash
cchq <env> update-supervisor-confs
```