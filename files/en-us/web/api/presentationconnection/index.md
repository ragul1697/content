---
title: PresentationConnection
slug: Web/API/PresentationConnection
page-type: web-api-interface
status:
  - experimental
browser-compat: api.PresentationConnection
---

{{SeeCompatTable}}{{securecontext_header}}{{APIRef("Presentation API")}}

The **`PresentationConnection`** interface of the [Presentation API](/en-US/docs/Web/API/Presentation_API) provides methods and properties for managing a single presentation. Each [presentation connection](https://www.w3.org/TR/presentation-api/#dfn-presentation-connection) is represented by a `PresentationConnection` object. Both the [controlling user agent](https://www.w3.org/TR/presentation-api/#dfn-controlling-user-agent) and [receiving user agent](https://www.w3.org/TR/presentation-api/#dfn-receiving-user-agent) _MUST_ implement `PresentationConnection`.

{{InheritanceDiagram}}

## Instance properties

- {{domxref("PresentationConnection.binaryType")}} {{Experimental_Inline}}
  - : Returns either blob or arrayBuffer. When a `PresentationConnection` object is created, its [`binaryType`](https://www.w3.org/TR/presentation-api/#idl-def-presentationconnection-binarytype) IDL attribute _MUST_ be set to the string [`"arraybuffer"`](https://www.w3.org/TR/presentation-api/#dom-binarytype-arraybuffer).
- {{domxref("PresentationConnection.id")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : Provides the presentation connection identifier.
- {{domxref("PresentationConnection.state")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : Returns the [presentation connection](https://www.w3.org/TR/presentation-api/#dfn-presentation-connection)'s current state.
- {{domxref("PresentationConnection.url")}} {{ReadOnlyInline}} {{Experimental_Inline}}
  - : Returns the URL used to create or reconnect to the presentation.

## Instance methods

- {{domxref("PresentationConnection.close()")}} {{Experimental_Inline}}
  - : Closes the current connection and sends a {{domxref("PresentationConnectionCloseEvent")}} to {{DOMxRef("PresentationConnection/close", "close")}} event.
- {{domxref("PresentationConnection.send()")}} {{Experimental_Inline}}
  - : Sends either binary or text data between a controlling browsing context and a presenting browsing context.
- {{domxref("PresentationConnection.terminate()")}} {{Experimental_Inline}}
  - : Terminates the current connection and fires {{domxref("PresentationConnection/terminate_event", "terminate")}} event.

## Events

- {{domxref("PresentationConnection/close_event", "close")}} {{Experimental_Inline}}
  - : Fired when there is a call to {{DOMxRef("PresentationConnection.close", "PresentationConnection.close()")}}.
- {{domxref("PresentationConnection/connect_event", "connect")}} {{Experimental_Inline}}
  - : Fired when a presentation connection is established.
- {{domxref("PresentationConnection/message_event", "message")}} {{Experimental_Inline}}
  - : Fired when there is a call to {{DOMxRef("PresentationConnection.send", "PresentationConnection.send()")}}.
- {{domxref("PresentationConnection/terminate_event", "terminate")}} {{Experimental_Inline}}
  - : Fired when there is a call to {{DOMxRef("PresentationConnection.terminate", "PresentationConnection.terminate()")}}.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
