# Sales ETL Pipeline with SQL Server Integration Services

This portfolio project demonstrates a batch ETL workflow using SSIS packages, a Visual Studio solution, project parameters, and data-flow/control-flow diagrams. It is a reproducible design/demo, not a deployed production catalog.

## Package inventory

The `ETL/` directory contains the `.dtsx` packages, `ETL.dtproj`, project parameters, and the SQL Server database project. The existing package filename `SSISpRroject.dtsx` is retained to avoid breaking solution references; rename it only together with matching references in the SSIS project.

## Local setup

Use Windows with Visual Studio and the SQL Server Integration Services Projects extension. Open `ETL.sln`, configure source and destination connection managers, review `Project.params`, and confirm the destination schema exists before execution. No credentials belong in Git.

## Validation and reruns

Before running a package, record source and destination schemas and expected row counts. After each package, capture inserted, rejected, and error-row counts. For a production extension, add package logging, error outputs, notifications, and an idempotent load key or staging-and-merge strategy so reruns cannot duplicate facts. A sample database is intentionally not committed; provide a sanitized local fixture before claiming end-to-end reproducibility.

## Limitations

The repository does not include a public sample database, deployed SSIS catalog, automated package execution, or a verified cloud deployment.
