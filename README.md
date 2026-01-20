# User Access Review and Account Reconciliation (Excel)

This project demonstrates how Microsoft Excel can be used to support Identity and Access Management (IAM) and access review activities by reconciling HR employee data with system user access lists.

The goal is to identify terminated employees who still have active system access and to summarise access removal actions across systems.

## Data Sources

- **HR_Employees**  
  Contains employee ID, name, department, employment status, and termination date.

- **System_Users**  
  Contains employee ID and system access assignments (e.g. VPN, M365, SAP, CRM).

> All data in this project is fictional and used for demonstration purposes only.

## Approach

1. **Reconciliation using XLOOKUP**  
   Employee IDs from HR records are matched against system user lists to identify existing access.

2. **Access Review Logic**  
   IF logic is used to classify each user as:
   - **OK** – Active employee with appropriate access  
   - **Terminated but has access** – Access removal required

3. **Visual Flagging**  
   Conditional formatting highlights terminated users who still have access.

4. **Pivot Table Reporting**  
   Pivot tables are used to:
   - Summarise how many access removals are required
   - Identify which systems are most impacted by terminated users

## Key Output

- **Access review table** showing user-level decisions (retain vs remove access)
- **Access removal summary pivot** showing the number of access removal actions per system

The pivot table represents access assignments, not unique users. One user with multiple systems appears multiple times, reflecting real-world access cleanup tasks.

---

## Skills Demonstrated

- Microsoft Excel (XLOOKUP, IF logic)
- Pivot Tables for access review reporting
- Identity and Access Management (IAM) fundamentals
- User offboarding and access cleanup analysis
- Audit and compliance-oriented documentation

---

## Notes

This project focuses on analysis and reporting. Actual access removal would be performed in the respective systems (e.g. Active Directory, VPN, SaaS applications) outside of Excel.

## Screenshots

The following screenshots provide a visual walkthrough of the Excel-based access review and account reconciliation process.

### Access Review Logic (IF Function)
![Access review IF logic](01_access_review_If_logic.png)

### System User Access List
![System users list](02_system_users_list.png)

### Systems to Close Identified Using XLOOKUP
![Systems to close XLOOKUP](03_systems_to_close_xlookup.png)

### Access Review Summary (Pivot Table)
![Access review pivot](04_access_review_pivot.png)

### Access Removal Summary (Operational Pivot)
![Access removal pivot](05_access_removal_pivot.png)
