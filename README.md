# ic-ruby-guide

# Controller & View
# Une seule variable @response affecté à la vue
- *Règle* :
Le controller retourne une seule variable à la vue (variable @response, de type hash).

*bad* : 
```
 @redirect_url = response[:redirect_url
 @success = response[:success_url]
 @fail = response[:fail_url]
 @abort = response[:abort_url]
 ```
*good*:
```
 @response = { 
   redirect: response[:redirect_url],
   success: response[:success_url],
   fail: response[:fail_url],
   abort: response[:abort_url] 
 }
```
