---
title: start_url
slug: Web/Manifest/start_url
page-type: web-manifest-member
browser-compat: html.manifest.start_url
---

{{QuickLinksWithSubpages("/en-US/docs/Web/Manifest")}}

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Type</th>
      <td><code>String</code></td>
    </tr>
  </tbody>
</table>

The `start_url` member is a string that represents the _start URL of the web application_ — the preferred URL that should be loaded when the user launches the web application (e.g., when the user taps on the web application's icon from a device's application menu or homescreen).

A valid `start_url` needs to be same-origin with the document that references the manifest. If `start_url` is unspecified or invalid in any way (such as not a string, not a valid URL, or not a same-origin with the document), the document URL is used.

> **Note:** The `start_url` member is purely advisory, and a user agent may ignore it or allow the user to alter it at install time or afterwards.

## Examples

### Absolute URL

```json
"start_url": "https://example.com"
```

### Relative URL

If the URL is relative, the manifest URL is used as the base URL to resolve it.

```json
"start_url": "../startpoint.html"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
