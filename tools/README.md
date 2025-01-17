# Tools

This directory includes auxiliary tools to support authoring and maintaining the Codacy documentation.

Install the Python requirements before using the tools:

```bash
pip3 install -r requirements.txt
```

## check-security-tools

Validates if the source file for the page [Security Monitor](https://docs.codacy.com/repositories/security-monitor/) mentions the tools returned by the Codacy API endpoint [listTools](https://api.codacy.com/api/api-docs#codacy-api-tools) that include security code patterns.

```bash
./check-security-tools.py
```

This script is scheduled to [run periodically as a GitHub Action](https://github.com/codacy/docs/actions/workflows/checks.yml).

## check-supported-tools

Validates if the source file for the page [Supported languages and tools](https://docs.codacy.com/getting-started/supported-languages-and-tools/) mentions the tools returned by the Codacy API endpoint [listTools](https://api.codacy.com/api/api-docs#codacy-api-tools).

```bash
./check-supported-tools.py
```

This script is scheduled to [run periodically as a GitHub Action](https://github.com/codacy/docs/actions/workflows/checks.yml).

## find-orphan-images.sh

Outputs a list of images that aren't included in any Markdown file.

```bash
./find-orphan-images.sh
```

## get-tool-descriptions

Outputs the name and description of each supported tool.

```bash
./get-tool-descriptions.py
```

## list-last-modified

Outputs the date and time when each documentation page was last modified. This can be used to help assess which pages could be outdated and in need of review.

```bash
./list-last-modified.py
```

## list-tool-short-names

Outputs the list of short names for all supported tools as returned by the Codacy API endpoint [tools](https://api.codacy.com/api/v3/tools). Useful to update and synchronize the list of tools in [Which tools can be configured and which name should I use?](https://docs.codacy.com/repositories-configure/codacy-configuration-file/#which-tools-can-be-configured-and-which-name-should-i-use).

```bash
./list-tool-short-names.sh
```
