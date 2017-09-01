# ic-ruby-guide

# Controller & View
## Une seule variable @response affecté à la vue
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

# Liens :
https://github.com/gauthier-delacroix/ruby-style-guide/blob/master/README-frFR.md

https://github.com/bbatsov/rails-style-guide#controllers

https://www.sitepoint.com/10-ruby-on-rails-best-practices-3/

http://pathfindersoftware.com/2008/10/elements-of-ruby-style/

Fonctionnal programming :

https://vimeo.com/75181845
