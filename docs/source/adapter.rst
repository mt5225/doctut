Introduce
=============
- adapters are exposed as RESTful API
- common headers ::
    
    St2-Api-Key: Y2YyYWJkOGFkNDgxYTdiZDI0ZDdjNzU1NmE0NzA2ZWJiYTBlNTE5YmJlOTg1ODU0MzNmNjc3MzcxNDE0MDFhZA
    content-type: application/json

- all calls are *Async*, call will return right away with task ID
- use task ID to query task status, for instance: ::

    curl -k -H "St2-Api-Key: Y2YyYWJkOGFkNDgxYTdiZDI0ZDdjNzU1NmE0NzA2ZWJiYTBlNTE5YmJlOTg1ODU0MzNmNjc3MzcxNDE0MDFhZA" -H "content-type: application/json" https://192.168.1.212/api/executions/56a53236b29f785a86436d0c


SSH Adapter
^^^^^^^^^^^^
- method: POST
- request sample: 

.. code-block:: json 

   {
     "action":"core.remote",
      "parameters":{
      "username":"root",
      "password":"root",
      "cmd":"df -h",
      "hosts":"192.168.1.212"
     }
   } 
