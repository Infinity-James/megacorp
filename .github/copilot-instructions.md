# MegaCorp Repository Guide for AI Agents

This is a **Git learning repository** for the Boot.dev Git 2 course, containing mock corporate data with intentional merge conflicts and sensitive data for educational purposes.

## Project Architecture

- **Data Organization**: Customer data stored in multiple formats (CSV, markdown, unstructured text) across [customers/](customers/) directory
- **Security Testing**: Contains intentionally leaked PII/credit cards in [customers/unstructured.txt](customers/unstructured.txt) for security scanning exercises
- **Contributor Management**: Simple GitHub profile links stored in [contributors/](contributors/) as individual `.txt` files
- **Partner Tracking**: Basic partner list in [orgs/partners.txt](orgs/partners.txt)
- **Content**: Educational "slander" content in [slander.md](slander.md) referencing course instructors

## Key Development Patterns

### Security Scanning Workflow
Use [scripts/scan.sh](scripts/scan.sh) to detect sensitive data:
```bash
./scripts/scan.sh
# Searches for credit cards, SSNs, and phone numbers with colored output
```

### Shell Abstraction Pattern  
[scripts/apux.sh](scripts/apux.sh) wraps commands and replaces "bash" with "apux" in output:
```bash
./scripts/apux.sh some-command
# Useful for command output transformation demonstrations
```

## Data Structure Conventions

- **CSV Files**: Use `first_name,last_name,company,title` headers (see [customers/banned.csv](customers/banned.csv))
- **Unstructured Data**: Mixed format customer data intentionally messy for cleanup exercises
- **Merge Conflicts**: [customers/favs.md](customers/favs.md) contains intentional Git conflict markers for learning
- **Contributors**: Store as individual `.txt` files containing only GitHub profile URLs

## Git Learning Context

This repository demonstrates:
- Merge conflict resolution (see [customers/favs.md](customers/favs.md))
- Security scanning workflows
- Data organization patterns across multiple formats
- Intentional sensitive data for detection practice

## Working with Sensitive Data

The [customers/unstructured.txt](customers/unstructured.txt) file contains mock PII including:
- Credit card numbers (4111-xxxx-xxxx-xxxx pattern)  
- SSN format (xxx-xx-xxxx)
- Phone numbers (multiple formats)
- Mixed structured/unstructured customer records

Always use [scripts/scan.sh](scripts/scan.sh) before commits to demonstrate security scanning practices.

## File Naming Patterns

- Contributors: `{name}.txt` in [contributors/](contributors/)
- Customer data: Descriptive names (`all.csv`, `banned.csv`, `favs.md`, `unstructured.txt`)
- Scripts: Executable `.sh` files in [scripts/](scripts/)

When modifying this repository, maintain the educational Git learning context and preserve intentional issues for course demonstrations.