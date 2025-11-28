# COMMUNICATION CONTRACT
### ---Requesting Data---

- file: notification_requests.json
- format: JSON array of request objects

[ { "operation": "SEND", "data": { "message": "your message here", "status": "success" } } ]

- Operations and Data

  - SEND – sends a notification message to the main program.
  - message (required): the notification text to display.
  - status (optional, default "success"): indicates type/status of notification (e.g., "success" or "error").
    - The status field is included by default (include_status=True) but can be omitted if the main program sets include_status=False.

- Example Request Call:



[ { "operation": "SEND", "data": { "message": "Habit added successfully!", "status": "success" } } ]

### ---Receiving Data---

- file: notification_responses.json
- format: JSON array of response objects
- Generally includes a status and message. Responses mirror the notification request, confirming the message has been processed.

- Example Response Call:


  - with status:
[ { "status": "success", "message": "Habit added successfully!" } ]
  - without status:
[ { "message": "Custom notification without status" } ]
