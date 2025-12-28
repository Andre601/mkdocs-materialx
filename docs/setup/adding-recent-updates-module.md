---
status: new
---

# Add recent updates module

<!-- md:version 10.0.4 -->
<!-- md:plugin [document-dates] -->

You can add a list of recently updated documents anywhere in your document with a single line of code. This is ideal for sites **with a large number of documents**, so that **readers can quickly see what's new**.

![recently-updated](../assets/screenshots/recently-updated.png)

## Installation

This feature is provided by the plugin [document-dates], which should be installed first:

```bash
pip install mkdocs-document-dates
```

then configure the switch recently-updated in `mkdocs.yml`:

```yaml
- document-dates:
    ...
    recently-updated:
      limit: 10        # Limit the number of docs displayed
      exclude:         # Exclude documents you don't want to show
        - index.md
        - blog/*
      # template: templates/recently_updated_list.html
```

You can also install the plugin [mkdocs-recently-updated-docs] to use alone

  [document-dates]: https://github.com/jaywhj/mkdocs-document-dates
  [mkdocs-recently-updated-docs]: https://github.com/jaywhj/mkdocs-recently-updated-docs

## Configuration

The following configuration options are supported:

<!-- md:option recently-updated.limit -->

:   <!-- md:default `10` --> This option specifies the number of documents to be displayed.

<!-- md:option recently-updated.exclude -->

:   <!-- md:default `[]` --> This option specifies the documents to be excluded.

<!-- md:option recently-updated.template -->

:   <!-- md:default `None` --> This option specifies the path to the custom rendering template.

## Add to sidebar navigation

Download the sample template [nav.html](https://github.com/jaywhj/mkdocs-document-dates/blob/main/templates/overrides/partials/nav.html), and override this path `docs/overrides/partials/nav.html`

## Add anywhere in the document

Insert this line anywhere in your document:

```yaml
<!-- RECENTLY_UPDATED_DOCS -->
```

## Custom template

See [templates](https://github.com/jaywhj/mkdocs-recently-updated-docs/tree/main/mkdocs_recently_updated_docs/templates) directory
