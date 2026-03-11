

```mermaid
erDiagram
  shuttle_vehicle {
    string vin pk
    integer max_occupancy not null
  }

  shuttle_route {
    integer route_id pk
  }

  shuttle_stop {
    integer stop_id pk
  }

  shuttle_run {
    integer run_id
  }

```
