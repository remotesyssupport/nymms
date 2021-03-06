=============
Configuration
=============

More coming soon... here's an example of config.yaml::

    # can be defined on a task by task basis
    monitor_timeout: 15
    resources: /etc/nymms/resources.yaml
    region: us-east-1
    results_topic: nymms_results
    tasks_queue: nymms_tasks
    state_domain: nymms_state

    probe:
      queue_wait_time: 20
    # can be defined on a task by task basis
      max_retries: 3
    # can be defined on a task by task basis
      retry_delay: 10

    scheduler:
      interval: 60
      backend: nymms.scheduler.backends.yaml_backend.YamlBackend
      backend_args:
        path: /etc/nymms/nodes.yaml

    reactor:
      queue_wait_time: 20
      visibility_timeout: 30
      queue_name: reactor_queue
      handler_config_path: /etc/nymms/handlers
