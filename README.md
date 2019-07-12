# Initial app setup
- Add to development block: `gem 'rubocop', '~> 0.72.0', require: false`
- bundle
- create .rubocop.yml at the root directory
- open .rubocop.yml and copy the contents of [this link]() to this file
- create .rubocop_app_overrides.yml at the root directory
- open .rubocop_app_overrides.yml and set your Specific Ruby version (EX):
```
AllCops:
  TargetRubyVersion: 2.5
``` 
- Open CMD Line and run: rubocop --auto-gen-config --exclude-limit=1000000
	* The exclude-limit by default is set to 15. After 15 violations it starts turning off cops (We do not want this)
	* Generates .rubocop.yml and rubocop_todo.yml
	* rubocop_todo.yml silences all existing rubocop violations, EXCEPT for: Metrics/LineLength and Metrics/LineLength Violations 	
- Add this line to your gitignore: `.rubocop-https--*-yaml` (Ignores the cache file)
