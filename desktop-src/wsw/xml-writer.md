---
title: XML-Writer
description: Der XML-Writer ist eine API zum Ausgeben von XML. Im Kern schreibt ein XML-Writer jeweils einen XML-Knoten. es gibt jedoch zusätzliche hilfsapis, mit denen das Schreiben einer Sequenz von Knoten vereinfacht wird.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- XML Writer-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106339104"
---
# <a name="xml-writer"></a>XML-Writer

Der XML-Writer ist eine API zum Ausgeben von XML. Im Kern schreibt ein XML-Writer jeweils einen [XML-Knoten](xml-node.md) . es gibt jedoch zusätzliche hilfsapis, mit denen das Schreiben einer Sequenz von Knoten vereinfacht wird.


Die folgenden Arten von Writer-Ausgaben werden unterstützt:

-   [**Ein Puffer im Arbeitsspeicher codierter Bytes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Ein Datenstrom**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Ein [XML-Puffer](xml-buffer.md)

Die folgenden Rückrufe werden mit dem XML-Writer verwendet:

-   [**WS- \_ dynamischer \_ Zeichen folgen \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**WS- \_ Pull- \_ Bytes- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS- \_ Push- \_ Bytes- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS- \_ Schreib \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Die folgenden Enumerationen werden mit dem XML-Writer verwendet:

-   [**WS-Zeichen \_ Satz**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**WS \_ XML \_ Writer \_ - \_ Codierungstyp**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**Ausgabe des WS \_ XML \_ Writer- \_ Ausgabe \_ Typs**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**WS \_ XML \_ Writer- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Die folgenden Funktionen werden mit dem XML-Writer verwendet:

-   [**Wscopynode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**Wscreatewriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**Wsflushwriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**Wsfrewriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**Wsgetprefixfromnamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**Wsgetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**Wsgetschreiterproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**Wsmovewriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**Wspullbytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**Wspushbytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**Wssetoutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**Wssetoutputtbuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**Wssetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**Wsschreitearray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**Wsschreitebytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**Wswrite techars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**Wsschreiteendattribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**Wsschreiteendcdata**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**Wsschreiteendelta-Element**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**Wsschreitenode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**Wsschreitequalifiedname**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**Wsschreitestartattribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**Wsschreitestartcdata**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**Wsschreitestartelements**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**Wsschreitetext**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**Wsschreitevalue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**Wsschreitexmlnsattribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

Der folgende Handle wird mit dem XML-Writer verwendet:

-   [WS- \_ XML- \_ Writer](ws-xml-writer.md)

Die folgenden Strukturen werden mit dem XML-Writer verwendet:

-   [**\_binäre WS XML \_ Writer- \_ \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**Ausgabe des WS \_ XML \_ Writer- \_ Puffers \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**WS- \_ XML- \_ Writer- \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**WS \_ XML \_ Writer- \_ MTOM- \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**Ausgabe des WS \_ XML \_ Writer \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**Eigenschaften von WS \_ XML \_ Writer \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**WS \_ XML \_ Writer ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**Ausgabe des WS \_ XML \_ Writer- \_ Streams \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**WS \_ XML \_ Writer- \_ Text \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




