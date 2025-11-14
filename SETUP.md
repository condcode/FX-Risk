# Setup Documentation

Tracking Databricks and AWS setup for future reference.

---

## 📋 Table of Contents
- [Databricks Setup and AWS Setup]

---

## 🔷 Databricks and AWS initial Setup

### Steps
- Setup account at aws and databricks. 
    -Create a Databricks workspace (FX Project) - Region: ca-central-1 (Canada Central)
-
- Free aws trial for databricks, auto configure
- Setup S3 buckets and structure
- Console at https://ca-central-1.console.aws.amazon.com/
- Setup policy and role . Role with access databricks account ID and external ID - 414351767826 is the account ID for databricks broadly (most applicable regions)
-trust policy on role should point to         "AWS": "253240084477"
- 1 policy for deployment access ec2 
- 1 policy for  with json to get, put, delete directed at main bucket and sub files
--You can set up a location through a connection or through credentials. Once you have credentials/connection you create an external location and you can autocreate all the profiles and linkages from here. For some reason it didnt create the role I needed on the aws side and I had to go there and add the role and correct permissions in the json. Quick check if you hit a bump.
-Make sure external location is added under catalog
-on the account module for databricks. configure storage for unity items storage
-
-open notebook and confirm locations and connections





### AWS Tables Created
| Table Name | Purpose | Schema |
|------------|---------|--------|
|     raw       |         |        |
|            |         |        |


### Useful Commands
```bash
# Test Databricks connection
databricks clusters list

# Test AWS connection
aws s3 ls

# Check Python packages
pip list | grep databricks
```

### Resources & Links
- Databricks Documentation: https://docs.databricks.com/
- AWS Documentation: https://docs.aws.amazon.com/


---

## 📝 Setup Checklist Summary

- [ ] Databricks account created and configured
- [ ] AWS account created and configured
- [ ] Databricks cluster running
- [ ] Database and tables created
- [ ] AWS IAM user configured
- [ ] Connection between Databricks and AWS established
- [ ] Python environment set up
- [ ] Tested data ingestion
- [ ] All credentials stored securely

---



---

_Last updated: [Nov13]_