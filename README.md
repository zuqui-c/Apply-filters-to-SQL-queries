# SQL Filtering for Security Investigations

## Project Description
This project demonstrates how SQL filtering techniques were applied to investigate potential security issues within an organization. The queries focus on identifying:
- Failed login attempts
- Unusual access times
- Location-based anomalies
- Department-specific employee data

These filters support internal security investigations and help improve incident response and threat detection.

---

## SQL Queries and Use Cases

### 1. Retrieve After-Hours Failed Login Attempts
This query selects all failed login attempts (`success = 0`) that occurred after 6:00 PM.

```sql
SELECT * 
FROM log_in_attempts 
WHERE success = 0 AND login_time > '18:00';


