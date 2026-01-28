# Summary: Failed SSH Login Analysis in Splunk

## Objective

To identify potential brute-force attacks on the `root` account by analyzing failed login attempts in the `secure.log` file.

## Query Overview

We used the following SPL query to detect failed SSH login attempts:

```spl
index="main" host=mailsv source="tutorialdata.zip:./mailsv/secure.log" sourcetype="secure-2" fail* root
