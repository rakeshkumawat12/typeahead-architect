Typeahead

What not to build. 
Autocomplete is available in many different settings.  
1. Smartphone Keyboards: word completion / contacts/.. 
2. Text editors / Code editors:  
a. intellisense: complete next token.  
b. Github CoPilot: can show entire functions
3. Grammarly: sentence completion while prose writing
4. Gmail / Outlook:
a. sentence completion for writing mail
b. to/cc/bcc: email completion from contacts


Key difference b/w Typeahead & Autocomplete  
Autocomplete is typically local to your machine. Any suggestions are specific to you. Autocomplete is standalone.   
Typeahead is always associated with search.  
The list of suggestions in typeahead are the most popular queries searched globally in the past, that match the given prefix.

Exciladraw img

Users are constantly searching on Google.  
Every time a user makes a search (search_query).  
• this search_query goes to the /search microservice   
• search microservice will return the relevant web-results   
• (async) the search microservice will inform the /typeahead microservice that this search has been made (pass the search_query)   
• the /typeahead service can store this search_query to populate its suggestions list