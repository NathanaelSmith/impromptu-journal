# Impromptu Journal Schema

### Tables
#### Users 
``` 
    user_id PRIMARY_KEY    id of user
    username          name of user
    firstname         first name of user
    lastname          last name of user
    password          password for the user
    display_prompts   preference to show journal prompts
```

#### Entries 
``` 
    id PRIMARY_KEY    id of journal entry
    entrycontent           content of journal entry
    latitude          latitude of location when entry made
    longitude         longitude of location when entry made
    timestamp         time entry was created
    prompt_id         id of prompt that prompted the entry
    user_id           id of user who created the entry
    
    FOREIGN_KEY prompt_id --> Prompts
    FOREIGN_KEY user_id --> Users
```

#### Prompts 
``` 
    prompt_id PRIMARY_KEY    id of prompt
    promptcontent           content of prompt
```

### Entities that tables represent

### Table Name Explanation/Relationship of entities/Normalization 
``` 
    Table Names Explained:
    Users       Simply called this because the subject of the table is the users.
    Entries     The subject of this table is the entries that the user is writing.
    Prompts     The subject of this entry is the prompt for the user.
    
    The tables are related in the following way:
        Entries have forien keys to both the Propmts table and the Users table. In this way, a user can be joined with their associated entry to link those two tables together. The entries table can then be joined with the prompt table to gather the content of the prompt and link it back to the user. 
        
    Normalization
        The relations above are in 2nd normal form. The columns are atomic in every relation and they all rely upon the primary key.
        
```

