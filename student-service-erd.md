# Student Service - Entity Relationship Diagram (ERD)

```mermaid
erDiagram

    user {
      string cognito_uuid
      string email_address
    }

    student {
        int student_id pk
        string user_id fk
        string first_name
        string last_name
        date birth_date
        string email_address
        string phone_number
        int student_number
        int academic_level
        int academic_major
        string dormitory
    }

    student_address {
        int address_id pk
        int student_id fk
        string street
        string city
        string state
        string zip_code
    }

    parent_contact {
        int contact_id pk
        int student_id fk
        string first_name
        string last_name
        string relationship
        string email_address
        string phone_number
    }

    student ||--|| user : logs-in-as
    student ||--o{ student_address : has-one-or-more
    student ||--o{ parent_contact : has-one-or-more

```
