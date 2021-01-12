# sonarqube_permission_template

Provides a Sonarqube Permission template resource. This can be used to create and manage Sonarqube Permission
templates.

## Example: create a template

```terraform
resource "sonarqube_permission_template" "template" {
    name                = "Internal-Projects"
    description         = "These are internal projects"
    project_key_pattern = "internal.*"
}
```

## Argument Reference

The following arguments are supported:

- name - (Required) The name of the Permission template to create. Changing this forces a new resource to be created.
- description - (Optional) Description of the Template.
- project_key_pattern - (Optional) The project key pattern. Must be a valid Java regular expression.

## Attributes Reference

The following attributes are exported:

- id - The ID of the Permission template.

## Import

Templates can be imported using their ID

```terraform
terraform import sonarqube_permission_template.template ABC_defghij
```
