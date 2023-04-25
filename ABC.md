# Disaster Recovery Test Plan - Draft

## Objective

The objective of this disaster recovery test is to validate the ability of the Rubric backup system and SAN replication to restore critical virtual machines and databases in the event of a disaster.

## Scope

The scope of this test will include the following:

- Restore virtual machines from Rubric appliances
- Restore virtual machines from Azure using Rubric
- Restore virtual machines from SAN replication
- Restore SQL databases from Rubric appliances, Azure using Rubric, and SAN replication
- Restore active directory components from Rubric appliances, Azure using Rubric, and SAN replication

## Test Environment

The test will be conducted in a lab environment that simulates the production environment as closely as possible. The lab environment consists of the following:

- 5 Dell compute and storage servers running VMware
- Rubric backup system with replication to Azure
- SAN replication between sites
- MPLS network connecting the sites

## Test Scenarios

### Test 1: Restore from Rubric appliances

1. Select VM001 from Rubric backup appliance and restore to original location
2. Monitor progress of restore job in Rubric dashboard
3. Verify that VM001 is powered on and accessible
4. Perform functional tests to ensure that VM001 is working properly
5. Repeat steps 1-4 for VM002
6. Select DB001 from Rubric backup appliance and restore to original location
7. Monitor progress of restore job in Rubric dashboard
8. Verify that DB001 is accessible and that data is intact
9. Perform functional tests to ensure that DB001 is working properly
10. Repeat steps 6-9 for DB002

### Test 2: Restore from Azure using Rubric

1. Select VM001 from Rubric backup system and restore to Azure
2. Monitor progress of restore job in Rubric dashboard
3. Verify that VM001 is powered on and accessible in Azure
4. Perform functional tests to ensure that VM001 is working properly
5. Repeat steps 1-4 for VM002
6. Select DB001 from Rubric backup system and restore to Azure
7. Monitor progress of restore job in Rubric dashboard
8. Verify that DB001 is accessible and that data is intact
9. Perform functional tests to ensure that DB001 is working properly
10. Repeat steps 6-9 for DB002

### Test 3: Restore from SAN replication

1. Select VM001 from SAN replication and restore to original location
2. Monitor progress of restore job in destination SAN
3. Verify that VM001 is powered on and accessible
4. Perform functional tests to ensure that VM001 is working properly
5. Repeat steps 1-4 for VM002
6. Select DB001 from SAN replication and restore to original location
7. Monitor progress of restore job in destination SAN
8. Verify that DB001 is accessible and that data is intact
9. Perform functional tests to ensure that DB001 is working properly
10. Repeat steps 6-9 for DB002

## Test Validation

1. Verify that all stakeholders are satisfied with the results of the test
2. Document the results of the test and identify any areas for improvement
3. Update the disaster recovery plan as necessary
