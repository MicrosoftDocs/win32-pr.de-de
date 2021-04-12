---
title: XML-Reader
description: Der XML-Reader ist ein Cursor über einer Eingabe Quelle von XML. Im Kern liest ein XML-Reader jeweils einen XML-Knoten. es gibt jedoch zusätzliche hilfsapis, mit denen das Lesen einer Sequenz von Knoten vereinfacht werden kann.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- XML-Reader-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474656"
---
# <a name="xml-reader"></a>XML-Reader

Der XML-Reader ist ein Cursor über einer Eingabe Quelle von XML. Im Kern liest ein XML-Reader jeweils einen [XML-Knoten](xml-node.md) . es gibt jedoch zusätzliche hilfsapis, mit denen das Lesen einer Sequenz von Knoten vereinfacht werden kann.


Die folgenden Arten von Leser Eingaben werden unterstützt:

-   [**Ein Puffer im Arbeitsspeicher codierter Bytes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Ein Datenstrom**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Ein [XML-Puffer](xml-buffer.md)

### <a name="security"></a>Sicherheit

Der Reader überprüft, ob die Attribute, die für ein Element vorhanden sind, eindeutig sind. Die Zeit, die zum Ausführen dieser Überprüfung erforderlich ist, ist eine Funktion der Anzahl von Attributen für das Element, die so groß wie die Attribute "Max" der [**WS \_ XML \_ Reader- \_ Eigenschaft \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)sein kann. Daher kann es vorkommen, dass große Dokumente verarbeitet werden, wenn die **\_ \_ \_ Eigenschaft \_ Max \_ Attribute der WS XML-Reader-Eigenschaft** auf einen großen Wert festgelegt ist.

Der Reader ordnet Namespaces Präfixe für jedes Element und jedes Attribut zu. Die Zeit, die zum Ausführen dieser Zuordnung erforderlich ist, ist eine Funktion der Anzahl von xmlns-Attributen im Bereich, die möglicherweise so groß wie die maximale Anzahl von [**\_ \_ \_ \_ \_ Namespaces der WS XML-Reader-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)ist Daher kann die Verarbeitung großer Dokumente, wenn diese Eigenschaft auf einen hohen Wert festgelegt ist, eine Gelegenheit für einen Denial-of-Service-Angriff darstellen.

Während der Reader sicherstellt, dass das Dokument der grammatikalen Spezifikation von XML folgt und die zugehörigen Aspekte in den angegebenen Kontingenten liegen, muss der Inhalt des Dokuments weiterhin als nicht vertrauenswürdig eingestuft werden, wenn er von einer nicht vertrauenswürdigen Quelle stammt. Benutzer des Readers sollten alle Element-und Attributnamen und Namespaces mithilfe von [**wslesetostartelement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**wsfindattribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)oder durch Manuelles Überprüfen von [**Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)überprüfen.

Einige andere zu berücksichtigende Situationen sind u. a. die folgenden:

-   Erwartete Elemente fehlen möglicherweise.
-   Unerwartete Elemente werden möglicherweise angezeigt.
-   Möglicherweise fehlen Attribute.
-   Unerwartete Attribute können angezeigt werden.
-   Elemente können als leere Elemente angezeigt werden.
-   Leerräume werden möglicherweise an unerwarteten Stellen angezeigt

Benutzer des Readers sollten keinen Speicher basierend auf den aus dem Dokument gelesenen Werten zuordnen. Sehen Sie sich beispielsweise das folgende XML-Dokument an:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Die Zuweisung eines Array basierten Soley in der Annahme, dass eine bestimmte Anzahl von Elementen befolgt wird, wäre ein potenzieller Angriffsvektor. Der Benutzer des Readers sollte in diesem Fall stattdessen den Arbeitsspeicher inkrementell zuweisen, wenn die Elemente angezeigt werden.

Der XML-Reader unterstützt DTD nicht. Der Benutzer des Readers muss sich nicht mit der DTD-Überprüfung befassen.

Der folgende Rückruf wird bei XML-Lesern verwendet:

-   [**WS- \_ Lese \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Die folgenden Enumerationen werden mit XML-Lesern verwendet:

-   [**WS- \_ XML- \_ \_ \_ lesecodierungstyp**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_ \_ \_ Eingabe \_ Typen des WS XML-Readers**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**Eigenschaften-ID der WS XML- \_ \_ Reader \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Die folgenden Funktionen werden mit XML-Lesern verwendet:

-   [**Wscreatereader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**Wsfillreader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**Wsfindattribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**Wsfreereader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**Wsgetnamespacefromprefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**Wsgetreadernode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**Wsgetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**Wsgetreaderproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**Wsgetxmlattribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**Wsmovereader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**Wslesarray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**Wslebytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**Wsleserchars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**Wsumdattribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**Wsleserumdelta**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**Wsread Node**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**Wsleserqualifiedname**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**Wsleserstartattribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**Wsleserstartelements**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**Wsumstartelements**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**Wsread Value**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**Wssetinput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**Wssetinputstobuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**Wssetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**Wsskipnode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

Das folgende Handle wird bei XML-Lesern verwendet:

-   [WS- \_ XML- \_ Reader](ws-xml-reader.md)

Die folgenden Strukturen werden mit XML-Lesern verwendet:

-   [**\_ \_ \_ Binär \_ Codierung des WS XML-Readers**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**WS- \_ XML- \_ Reader- \_ Puffer \_ Eingabe**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**WS- \_ XML- \_ Reader- \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**WS- \_ XML- \_ Reader- \_ Eingabe**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**WS- \_ XML- \_ Reader- \_ MTOM- \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**Eigenschaften des WS- \_ XML- \_ Readers \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**WS \_ XML \_ Reader ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**WS \_ XML \_ Reader \_ Stream- \_ Eingabe**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**WS- \_ XML- \_ Reader- \_ Text \_ Codierung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




