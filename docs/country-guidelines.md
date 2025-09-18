# Country-Specific Data Guidelines

## Adding Contact Details of Officials

### Finding Information
1. **Official Government Portals**: Check official government websites for contact details of officials.
2. **Public Records**: Use publicly available records and verified sources.

### Adding Contact Details
1. **Create Directories**: Follow the structure `data/country/{country-name}/contacts/{office-type}`.
2. **JSON Template**: Use the standard JSON template to add contact details for each official.
3. **File Naming Convention**: Use the official's name in the file name, formatted as `{official-name}.json`.

### Example JSON Template
```json
{
  "name": "John Doe",
  "position": "Representative",
  "office": "House of Representatives",
  "country": "Nigeria",
  "phone": "+234-123-456-7890",
  "email": "john.doe@example.com",
  "address": {
    "office_address": "123 Government Building, Abuja, Nigeria",
    "postal_code": "12345"
  },
  "social_media": {
    "twitter": "@JohnDoe",
    "facebook": "facebook.com/JohnDoe"
  },
  "term_start": "2023-01-01",
  "term_end": "2027-01-01"
}
