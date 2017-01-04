# RESTFUL challenge SOLUTION

### Kickstarter
Welcome to Kickstarter. Assume we have a model called `Project` that inherits from `ActiveRecord::Base`, a corresponding table called `projects`, and a controller called `ProjectsController` that inherits from `ApplicationController`

For each of the following descriptions, write out the corresponding:

1. The HTTP Verb and URL (ie 'GET '/posts'')
2. The rails controller action (ie 'posts#index')
3. The corresponding CRUD action (ie 'READ)
4. The corresponding ActiveRecord method (ie 'all')
5. The corresponding SQL (ie 'SELECT * FROM posts')

### Actions

#### Displays all of the projects
  1. GET '/projects'
  2. 'projects#index'
  3. READ
  4. `Project.all`
  5. 'SELECT * FROM projects'
#### Displays information about one project
  1. GET '/projects/:id'
  2. 'projects#show'
  3. READ
  4. `Project.find(params[:id])`
  5. 'SELECT * FROM projects WHERE id = ?'
#### Displays a form to create a new project
  1. GET '/projects/new'
  2. 'projects#new'
  3. none - just shows a form
  4. `Project.new` if you're using `form_form`
  5. none - just shows a form
#### Creates a new project based on given parameters
  1. POST '/projects'
  2. 'projects#create'
  3. CREATE
  4. `Project.create(project_prams)`
  5. INSERT INTO projects VALUES (?, ?, ?)
#### Displays a form to update an existing project
  1. GET '/projects/:id/edit'
  2. 'projects#edit'
  3. none - just displays a form
  4. `Project.find(params[:id])` - has to find which project to update
  5. `SELECT * FROM projects WHERE id = ?`
#### Updates an existing project with given parameters
  1. PATCH or PUT '/projects/:id'
  2. 'projects#update'
  3.  UPDATE
  4. `project = Project.find(params[:id])` - has to find which project to update
      `project.update(product_params)`
  5. `SELECT * FROM projects WHERE id = ?`
      `UPDATE products SET () WHERE id = ?`
#### Deletes an existing project
  1.  DELETE '/projects/:id'
  2. 'projects#destroy'
  3.  DELETE
  4. `project = Project.find(params[:id])` - has to find which project to destroy
      `project.destroy`
  5. `DELETE FROM projects WHERE id = ?`
