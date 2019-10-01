# Impromptu Journal Schema

### Tables
#### Users 
``` 
    id PRIMARY_KEY    id of user
    username          name of user
    display_prompts   preference to show journal prompts
```

#### Entries 
``` 
    id PRIMARY_KEY    id of journal entry
    content           content of journal entry
    latitude          latitude of location when entry made
    longitude         longitude of location when entry made
    timestamp         time entry was created
    prompt_id         id of prompt that prompted the entry
    user_id           id of user who created the entry
    
    FK prompt_id --> Prompts
    FK user_id --> Users
```

#### Prompts 
``` 
    id PRIMARY_KEY    id of prompt
    content           content of prompt
```
