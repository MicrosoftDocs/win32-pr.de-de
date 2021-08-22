---
title: XML Writer
description: XML Writer ist eine API zum Ausgeben von XML. Im Kern schreibt ein XML Writer jeweils einen XML-Knoten, aber es gibt zusätzliche Hilfs-APIs, um das Schreiben einer Sequenz von Knoten zu vereinfachen.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- XML Writer-Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75b7937ac6d8f6e9daff40289dd34729eaf235f203a02b91b5d1af3632049b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026058"
---
# <a name="xml-writer"></a>XML Writer

XML Writer ist eine API zum Ausgeben von XML. Im Kern schreibt ein XML Writer jeweils einen [XML-Knoten,](xml-node.md) aber es gibt zusätzliche Hilfs-APIs, um das Schreiben einer Sequenz von Knoten zu vereinfachen.


Die folgenden Arten von Writerausgaben werden unterstützt:

-   [**Ein In-Memory-Puffer codierter Bytes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Ein Stream**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Ein [XML-Puffer](xml-buffer.md)

Die folgenden Rückrufe werden mit dem XML-Writer verwendet:

-   [**WS \_ DYNAMIC \_ STRING \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_ \_ WS-PULLBYTERÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Die folgenden Enumerationen werden mit dem XML-Writer verwendet:

-   [**WS \_ CHARSET**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**WS \_ XML \_ \_ WRITER-CODIERUNGSTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**WS \_ XML \_ \_ WRITER-AUSGABETYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**WS \_ XML \_ \_ WRITER-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Die folgenden Funktionen werden mit dem XML-Writer verwendet:

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

Das folgende Handle wird mit dem XML-Writer verwendet:

-   [WS \_ XML \_ WRITER](ws-xml-writer.md)

Die folgenden Strukturen werden mit dem XML-Writer verwendet:

-   [**BINÄRE WS \_ XML \_ \_ \_ WRITER-CODIERUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**WS \_ XML \_ WRITER \_ BUFFER \_ OUTPUT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**WS \_ XML \_ \_ WRITER-CODIERUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**WS \_ XML \_ WRITER \_ MTOM \_ ENCODING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**WS \_ XML \_ \_ WRITER-AUSGABE**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**WS \_ XML \_ \_ WRITER-EIGENSCHAFTEN**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**WS \_ XML \_ \_ WRITER-EIGENSCHAFT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**AUSGABE DES WS \_ XML \_ \_ WRITER-STREAMS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**WS \_ XML \_ \_ WRITER-TEXTCODIERUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




