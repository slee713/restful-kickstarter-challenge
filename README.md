# RESTFUL challenge

### Kickstarter
Welcome to Kickstarter. Assume we have a model called `Project` that inherits from `ActiveRecord::Base`, a corresponding table called `projects`, and a controller called `ProjectsController` that inherits from `ApplicationController`

For each of the following descriptions, write out the corresponding:

1. The HTTP Verb and URL (ie 'GET '/dogs'')
2. The rails controller action (ie 'dogs#index')
3. The corresponding CRUD action (ie 'READ)
4. The corresponding ActiveRecord method (ie 'all')


### Actions

1. Displays all of the projects
    - get '/projects', to: "projects#index", (projects_path)
2. Displays information about one project
    - get '/projects/:id', to: "projects#show", (project_path)
3. Displays a form to create a new project
    - get '/projects/new', to: "projects#new", (new_project_path)
4. Creates a new project based on given parameters
    - post '/projects', to: "projects#create", 
5. Displays a form to update an existing project
    - get '/projects/:id/edit', to: "projects#edit", (edit_project_path)
6. Updates an existing project with given parameters
    - patch '/projects/:id', to: "projects#patch", 
7. Deletes an existing project
    - delete '/projects/:id', to: 'projects#destroy',
