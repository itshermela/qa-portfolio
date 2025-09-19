# Bug Report: Login allows invalid email format

**Steps to Reproduce:**
1. Go to login page
2. Enter email as `user@invalid` and any password
3. Click Login

**Expected Result:**
Validation error should appear for invalid email.

**Actual Result:**
Login request is sent to backend.

**Severity:** Medium  
**Priority:** P2
