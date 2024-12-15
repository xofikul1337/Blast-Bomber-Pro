# Blast-Bomber-Pro

# Blast Bomber Bot - API Body Documentation

This documentation explains how to integrate the `number` variable into the API body when performing message bombing with the Blast Bomber Bot.

### What is the `number` variable?
The `number` variable holds the 11-digit mobile number you input for the bot to send messages. When submitting an API body, the `number` variable replaces the actual mobile number, ensuring the bot receives the correct number.

**Important Notes:**
- Do not enclose the `number` in quotation marks (i.e., `"number"` is incorrect).
- Ensure that the `number` variable is inserted correctly in the API body.

### Example API Body Format

1. **With `+88` or `88` prefix:**

   Example API Body:
   ```json
   {
     "email": "example@gmail.com",
     "phone_number": "8801945284"
   }
   ```
   Change the phone number field to:
   ```json
   {
     "email": "example@gmail.com",
     "phone_number": "88" +number
   }
   ```

2. **Without prefix (plain 11 digits):**

   Example API Body:
   ```json
   {
     "phone_number": "01844445862"
   }
   ```
   Change the phone number field to:
   ```json
   {
     "phone_number": number
   }
   ```

3. **With `+88` prefix and additional fields:**

   Example API Body:
   ```json
   {
     "phone_number": "+8801924981783",
     "sent": "success",
     "result": "true"
   }
   ```
   Change the phone number field to:
   ```json
   {
     "phone_number": "+88" +number,
     "sent": "success",
     "result": "true"
   }
   ```

### Key Points:
- Replace the mobile number with `number` in the body of the API.
- For any prefix like `+88`, keep it enclosed in quotes and append `+number`.
- For direct 11-digit numbers, remove the quotes and just insert `number`.

---

This brief README explains the usage and proper formatting of the `number` variable for API integration with the Blast Bomber Bot.
