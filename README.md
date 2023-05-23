# git_test_release
for testing automation in github
Project monthly release cut automation:
1)In jenkins: Disable azuremonthlybranch job

2)Manual steps for one repo:
2.1) lock the monthly branch
2.2) get the latest commit id and create tag using that with the format of YYYYMMDD_monthly
2.3) verify tag is created
2.4) delete monthly branch
2.5) create monthly branch from master
2.6) verify the commit id of monthly, should be same as master commit id

3) Manual changes
  3.1)In o9platform > deploy > build.description 
           build discription YYYYMM
  3.2)nifi-dev-repo > tests > gitmodules >> branch : monthly
  3.3) creating new branch from master in o9servicesk8 according to format monthly-YYYYMM
  
4) In jenkins: enable azuremonthlybranch job
