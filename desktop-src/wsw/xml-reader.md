---
title: XML-Reader
description: DER XML-Reader ist ein Cursor über einer Eingabequelle von XML. Im Kern liest ein XML-Reader jeweils einen XML-Knoten, aber es gibt zusätzliche Hilfs-APIs, um das Lesen einer Sequenz von Knoten zu vereinfachen.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- XML Reader Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a03ef961cd49c481564b6bad1ad86603c9cb576f0c8aeda1a7cd2d6d18aaeef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770870"
---
# <a name="xml-reader"></a>XML-Reader

DER XML-Reader ist ein Cursor über einer Eingabequelle von XML. Im Kern liest ein XML-Reader jeweils einen [XML-Knoten,](xml-node.md) aber es gibt zusätzliche Hilfs-APIs, um das Lesen einer Sequenz von Knoten zu vereinfachen.


Die folgenden Typen von Readereingaben werden unterstützt:

-   [**Ein In-Memory-Puffer codierter Bytes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Ein Stream**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Ein [XML-Puffer](xml-buffer.md)

### <a name="security"></a>Sicherheit

Der Reader überprüft, ob die in einem Element vorhandenen Attribute eindeutig sind. Die zeitaufwendige Ausführung dieser Überprüfung ist eine Funktion der Anzahl von Attributen für das Element, die so groß sein kann wie [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Daher kann die Verarbeitung großer Dokumente, wenn **WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES** auf einen hohen Wert festgelegt ist, eine Möglichkeit für einen Denial-of-Service-Angriff darstellen.

Der Reader weist Namespaces präfixe für jedes Element und jedes Attribut zu. Die zeitaufwendige Zeit für diese Zuordnung ist eine Funktion der Anzahl von xmlns-Attributen im Gültigkeitsbereich, die so groß sein kann wie [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ NAMESPACES.**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id) Daher kann die Verarbeitung großer Dokumente, wenn diese Eigenschaft auf einen hohen Wert festgelegt ist, eine Möglichkeit für einen Denial-of-Service-Angriff darstellen.

Während der Reader sicherstellt, dass das Dokument der grammatikalischen Spezifikation von xml entspricht und darüber hinaus seine Aspekte innerhalb der angegebenen Kontingente liegen, muss der Inhalt des Dokuments immer noch als nicht vertrauenswürdig betrachtet werden, wenn er von einer nicht vertrauenswürdigen Quelle stammt. Benutzer des Readers sollten alle Element- und Attributnamen und Namespaces mithilfe von [**WsReadToStartElement,**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement) [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)oder durch manuelles Untersuchen von [**Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)überprüfen.

Einige andere zu berücksichtigende Situationen sind u. a.:

-   Erwartete Elemente fehlen möglicherweise
-   Unerwartete Elemente können angezeigt werden.
-   Erwartete Attribute fehlen möglicherweise
-   Unerwartete Attribute können angezeigt werden.
-   Elemente können als leere Elemente angezeigt werden.
-   Leerzeichen können an unerwarteten Stellen angezeigt werden.

Benutzer des Readers sollten keinen Speicher basierend auf einfachen Werten zuweisen, die aus dem Dokument gelesen werden. Betrachten Sie beispielsweise das folgende XML-Dokument:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Das Zuordnen eines Arrays basierend auf der Annahme, dass einige Elemente folgen werden, wäre ein potenzieller Angriffsvektor. Der Benutzer des Readers sollte in diesem Fall stattdessen den Arbeitsspeicher inkrementell zuordnen, wenn die Elemente angezeigt werden.

Der XML-Reader unterstützt DTD nicht. Der Benutzer des Readers muss sich keine Gedanken über die DTD-Überprüfung machen.

Der folgende Rückruf wird mit XML-Readern verwendet:

-   [**WS \_ READ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Die folgenden Enumerationen werden mit XML-Readern verwendet:

-   [**WS \_ XML READER ENCODING TYPE (WS-XML-READERCODIERUNGSTYP) \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_ \_ WS-XML-READEREINGABETYP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**WS \_ XML \_ READER \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Die folgenden Funktionen werden mit XML-Readern verwendet:

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

Das folgende Handle wird mit XML-Readern verwendet:

-   [\_WS-XML-READER \_](ws-xml-reader.md)

Die folgenden Strukturen werden mit XML-Readern verwendet:

-   [**BINÄRCODIERUNG DES \_ WS-XML-READERS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**WS \_ XML \_ READER \_ BUFFER \_ INPUT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_WS-XML-READERCODIERUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_WS-XML-READEREINGABE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**WS \_ XML \_ READER \_ MTOM \_ ENCODING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**WS \_ XML \_ READER \_ PROPERTIES**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_ \_ WS-XML-READER-EIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**EINGABE DES \_ WS-XML-READERSTREAMS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**\_WS-XML-READER- \_ \_ \_ TEXTCODIERUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




