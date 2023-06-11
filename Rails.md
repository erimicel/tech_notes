## Rails 7.0.5 New app
rails new myapp -d postgresql --css=tailwind --javascript=esbuild --skip-test --skip-jbuilder  --skip-action-text --skip-action-mailbox --skip-action-mailer --skip-active-storage

## ActionText

# In config/application.rb
config.action_view.sanitized_allowed_tags = ['strong', 'em', 'a']
config.action_view.sanitized_allowed_attributes = ['href', ‘id’, ‘title']

To allow or sanitize html attributes and tags

## Localization

### Date with l method and format => locales.yml
<%= l user.created_at, format: :short %>

## Credentials
EDITOR='code --wait' rails credentials:edit

## Routes
http://localhost:3000/rails/info/routes

## Database Queries

### RAILS: ORDER STRING AS INT WITH SQL
.order('ABS(CAST(number AS int))')

### SQL: extract year from date with sql 
MODEL.where("extract(year  from debit_date) = ?",Date.today.year)
