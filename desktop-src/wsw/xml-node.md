---
title: XML-Knoten
description: Ein XML-Knoten stellt ein einzelnes XML-Element dar, z. b. ein Start Element und seine Attribute, ein Endelement, Text oder \ 0034; typisiertes \ 0034; Text Inhalt, z. b. ein Integer-oder Byte-Array. Die Daten in einem Knoten variieren je nach dem Typ des WS- \_ XML- \_ Knotens \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- XML-knotenweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106337692"
---
# <a name="xml-node"></a>XML-Knoten

Ein XML-Knoten stellt ein einzelnes XML-Element dar, z. b. ein Start Element und seine Attribute, ein Endelement, Text oder einen "typisierten" Text Inhalt, z. b. eine ganze Zahl oder ein Bytearray. Die Daten in einem Knoten variieren je nach dem [**Typ des WS- \_ XML- \_ Knotens \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


Im folgenden finden Sie ein Beispiel für ein Codierungs spezifisches XML-Dokument, das mit codierten unabhängigen Strukturen dargestellt wird.

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

Die folgenden Enumerationen werden mit XML-Knoten verwendet:

-   [**WS \_ - \_ Werttyp**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**WS- \_ XML- \_ \_ Knotentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**WS- \_ XML- \_ \_ Texttyp**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Die folgenden Funktionen werden mit XML-Knoten verwendet:

-   [**Wstrimxmlwhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**Wsverifyxmlncname**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**Wsxmlstringequals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Die folgenden Makros werden mit XML-Knoten verwendet:

-   [**WS- \_ XML- \_ Zeichen folgen \_ \_ Wert**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**WS- \_ XML- \_ Zeichenfolge \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**WS- \_ XML- \_ Zeichen folgen \_ Wert**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Die folgenden Strukturen werden mit XML-Knoten verwendet:

-   [**WS- \_ XML- \_ Attribut**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**WS- \_ XML- \_ Base64- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**\_ \_ boolescher Text von WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**WS- \_ XML- \_ Kommentar \_ Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**WS \_ XML- \_ DateTime- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**WS \_ XML- \_ Dezimal \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**WS \_ XML- \_ Wörterbuch**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ doppelter \_ Text in WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**WS- \_ XML- \_ Element \_ Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**WS- \_ XML- \_ float- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**WS- \_ XML- \_ GUID- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**WS \_ XML \_ Int32 \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**WS \_ XML \_ Int64 \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**WS- \_ XML- \_ Listen \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**WS- \_ XML- \_ Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS- \_ XML- \_ QName**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**WS- \_ XML- \_ QName- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**WS \_ XML- \_ Zeichenfolge**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**WS- \_ XML- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**WS \_ XML- \_ Text \_ Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**WS \_ XML \_ TimeSpan- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**WS \_ XML \_ UINT64 \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**eindeutiger WS \_ XML- \_ ID- \_ \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**WS \_ XML \_ UTF16 \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**WS- \_ XML- \_ UTF8- \_ Text**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 