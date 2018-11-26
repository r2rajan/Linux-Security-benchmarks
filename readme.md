Please refer to this wiki page for documentation <br>
https://github.com/r2rajan/Linux-Security-benchmarks/wiki<br>

**Pre-requisites**
1. Install openscap 

`yum install openscap`

2. Install openscap scanner

`yum install openscap-scanner`

3. Install openscap utilities

`yum install openscap-utils`

4. Download the XCCDF data stream file and and tailored CIS profile (from this github page) and store them in /root <br>
**XCCDF Data Stream file** - ssg-rhel7-cis-ds.xml<br>
**Tailored - CIS profile** - CISprofile-tailor.xml<br>

**Usage**<br>

**Assessment** <br>

Command to perform as assessment and to generate a HTML report

` oscap xccdf eval --profile xccdf_org.cissecurity_profile_server --report /root/report.html --tailoring-file /root/CISprofile-tailor.xml /root/ssg-rhel7-cis-ds.xml`

**Remediation** <br>

Command performs an assessment and then remediates the failures based on the results of the assessment

` oscap xccdf eval --remediate --profile xccdf_org.cissecurity_profile_server --report /root/report.html --tailoring-file /root/CISprofile-tailor.xml /root/ssg-rhel7-cis-ds.xml`
