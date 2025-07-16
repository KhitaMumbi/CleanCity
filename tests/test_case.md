 Authentication System Test Cases
markdown
| ID     | Title                     | Steps                                                                 | Test Data                              | Expected Result                          | Priority |
|--------|---------------------------|-----------------------------------------------------------------------|----------------------------------------|------------------------------------------|----------|
| TC-001 | Valid Registration        | 1. Go to /register<br>2. Fill valid data<br>3. Submit                 | name="Test User"<br>email="test@example.com"<br>password="Pass123!"<br>confirm="Pass123!" | Redirect to /login, user in localStorage | High     |
| TC-002 | Password Mismatch         | 1. Enter different passwords<br>2. Submit                             | password="Pass123!"<br>confirm="Pass456!" | Error: "Passwords must match"            | High     |
| TC-003 | Valid Login               | 1. Enter correct credentials<br>2. Submit                             | email="user@cleancity.com"<br>password="password123" | Session created, redirect to /dashboard  | Critical |
| TC-004 | Invalid Login             | 1. Enter wrong credentials<br>2. Submit                               | email="wrong@email.com"<br>password="wrong" | Error: "Invalid credentials"             | High     |
| TC-005 | Admin Access Verification | 1. Login as admin<br>2. Check navigation                             | email="admin@cleancity.com"<br>password="admin123" | "Admin" link visible                     | Medium   |
🗑️ Waste Management Test Cases
markdown
| ID     | Title                     | Steps                                                                 | Test Data                              | Expected Result                          | Priority |
|--------|---------------------------|-----------------------------------------------------------------------|----------------------------------------|------------------------------------------|----------|
| TC-006 | Valid Pickup Request      | 1. Fill pickup form<br>2. Submit                                     | date=tomorrow<br>type=Recyclable<br>location=Nairobi | Success toast, request in dashboard      | High     |
| TC-007 | Past Date Validation      | 1. Set date to yesterday<br>2. Submit                                | date=yesterday                         | Error: "Date must be future"             | High     |
| TC-008 | Cancel Pending Request    | 1. Create request<br>2. Click cancel                                 | requestId="REQ001"                     | Status changes to "Cancelled"             | Medium   |
| TC-009 | Modify Pickup Details     | 1. Edit pickup before 24h window<br>2. Save                          | newDate=tomorrow+1day                  | Changes reflected in dashboard            | Medium   |
📊 Dashboard Test Cases
markdown
| ID     | Title                     | Steps                                                                 | Test Data                              | Expected Result                          | Priority |
|--------|---------------------------|-----------------------------------------------------------------------|----------------------------------------|------------------------------------------|----------|
| TC-010 | Dashboard Rendering       | 1. Login<br>2. Navigate to /dashboard                                | User with 5 requests                   | All requests displayed                   | Critical |
| TC-011 | Filter by Status          | 1. Select "Completed" filter                                         | 3 completed, 2 pending                 | Only 3 requests shown                    | Medium   |
| TC-012 | Data Export               | 1. Click "Export CSV"                                                | User with 10 requests                  | CSV file downloads                       | Low      |
📝 Content Management Test Cases
markdown
| ID     | Title                     | Steps                                                                 | Test Data                              | Expected Result                          | Priority |
|--------|---------------------------|-----------------------------------------------------------------------|----------------------------------------|------------------------------------------|----------|
| TC-013 | Awareness Page Load       | 1. Navigate to /awareness                                            | -                                      | All sections render properly             | Medium   |
| TC-014 | Quiz Completion           | 1. Answer all questions<br>2. Submit                                 | score=5/5                              | "Perfect score!" message                 | Low      |
👥 Community Features Test Cases
markdown
| ID     | Title                     | Steps                                                                 | Test Data                              | Expected Result                          | Priority |
|--------|---------------------------|-----------------------------------------------------------------------|----------------------------------------|------------------------------------------|----------|
| TC-015 | Create Community Post     | 1. Submit new post<br>2. Refresh feed                                | title="Test"<br>content="Hello World"  | Post appears in feed                     | Medium   |

