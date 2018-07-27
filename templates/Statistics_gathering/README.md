## template: Statistics gathering 

### Description:
This template is responsible for get statistics of node then add it in InfluxDB and Visualization in grafana

### Schema:

- `node`: Name of the node

### Actions
- `start`: starts the reporting every 5 minutes
- `stop`: stops the reporting


### Examples:
#### DSL (api interface):
```python
stat = robot.services.create('github.com/zero-os/0-templates/Statistics_gathering/0.0.1','1e2b8c6b-b5b9-42c1-99f4-f9149dc25743')
stat.schedule_action('start')
```

#### Blueprint (cli interface):
```yaml
services:
    - github.com/zero-os/0-templates/Statistics_gathering/0.0.1__1e2b8c6b-b5b9-42c1-99f4-f9149dc25743:

actions:
    - template: github.com/zero-os/0-templates/Statistics_gathering/0.0.1
      service: '1e2b8c6b-b5b9-42c1-99f4-f9149dc25743'
      actions: ['start']
```