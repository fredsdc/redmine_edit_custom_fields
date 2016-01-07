# Edit Custom Fields plugin for Redmine

This is a Redmine plugin to enable users editing issue custom fields for their project.

By default, Redmine provides the mechanism of creating custom fields to extend the
semantics of certain entities, e.g. issues or projects. The properties of these Custom
Fields can only be edited by a Redmine administrator making them often useless in
projects where a manager or another designated member has to be able to amend these
semantic fields.

This plugins enables users with the appropriate permissions to edit the custom fields
attached to issues within the current project.

## Features

* Allows editing of certain issue custom fields for a project.
* Allows to choose which custom fields are user-editable.
* Provides a new permission for user roles.
* Provides a new module permission for projects.

## Installation

For installation, clone the Git repository to your `plugins` folder, restart the Redmine application and perform the migration.

    cd redmine/plugins
    git clone https://github.com/fathomssen/redmine_edit_custom_fields.git
    rake redmine:plugins:migrate NAME=redmine_edit_custom_fields RAILS_ENV=production

## Configuration

After installing the plugin, you have to perform some configuration to enable this plugin for users and projects.

1. In the Administration area, open the "Roles and permissions" tab.
    1. Either choose an existing role or create a new one.
    2. In the Permissions area, check "Edit custom fields".
    3. Click on the Save button.
    4. Now, this user role is allowed to edit custom fields.
2. In the Settings tab of a project, open the Modules tab.
    1. Check "Edit custom fields".
    2. Click on the Save button.
    3. Now, a new tab "Custom fields" will have appeared.

## Todo

* Add a select box to choose which custom field to edit.
