erDiagram

    POINTS {
        INT point_id PK
        VARCHAR point_name
        TEXT location_desc
        TIMESTAMP created_at
    }

    ISSUES {
        INT issue_id PK
        INT point_id FK
        TEXT note
        VARCHAR status
        VARCHAR inspector
        TIMESTAMP created_at
    }

    POINTS ||--o{ ISSUES : "has"
