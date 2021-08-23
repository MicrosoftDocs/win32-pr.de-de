---
title: XML-Knoten
description: Ein XML-Knoten stellt ein einzelnes XML-Element dar, z. B. ein Startelement und seine Attribute, ein Endelement, Text oder \ 0034;typisiert \ 0034; Textinhalt, z. B. eine ganze Zahl oder ein Bytearray. Die Daten in einem Knoten variieren je nach \_ WS-XML-KNOTENTYP. \_ \_
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- XML-Knotenwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b851ad0ab0a6a333fedea13036eebf11e8c727a04603c07d8f7e68e66de5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545650"
---
# <a name="xml-node"></a>XML-Knoten

Ein XML-Knoten stellt ein einzelnes XML-Element dar, z. B. ein Startelement und seine Attribute, ein Endelement, Text oder "typisierter" Textinhalt, z. B. ein Integer- oder Bytearray. Die Daten in einem Knoten variieren je nach [**\_ WS-XML-KNOTENTYP. \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)


Das folgende Beispiel zeigt ein Codierungsspezifisches XML-Dokument, das mit Codierungsunabhängigen Strukturen dargestellt wird.

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

-   [**\_WS-WERTTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**WS \_ \_ \_ XML-KNOTENTYP**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**WS \_ \_ \_ XML-TEXTTYP**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Die folgenden Funktionen werden mit XML-Knoten verwendet:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Die folgenden Makros werden mit XML-Knoten verwendet:

-   [**WS \_ XML \_ STRING \_ DICTIONARY \_ VALUE**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**WS \_ XML \_ STRING \_ NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_ \_ WS-XML-ZEICHENFOLGENWERT \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Die folgenden Strukturen werden mit XML-Knoten verwendet:

-   [**\_WS-XML-ATTRIBUT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**WS \_ XML \_ BASE64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**WS \_ XML \_ BOOL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**\_WS-XML-KOMMENTARKNOTEN \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**WS \_ XML \_ DATETIME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**WS \_ XML \_ DECIMAL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**\_ \_ WS-XML-WÖRTERBUCH**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**WS \_ XML \_ DOUBLE \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**WS \_ \_ \_ XML-ELEMENTKNOTEN**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**WS \_ XML \_ FLOAT \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**\_ \_ WS-XML-GUID-TEXT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**WS \_ XML \_ INT32 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**WS \_ XML \_ INT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**WS \_ XML \_ LIST \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_WS-XML-KNOTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS \_ XML \_ QNAME**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**WS \_ XML \_ QNAME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**WS \_ XML \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_WS-XML-TEXTKNOTEN \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**WS \_ XML \_ TIMESPAN \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**WS \_ XML \_ UINT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**EINDEUTIGER \_ \_ WS-XML-ID-TEXT \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**WS \_ XML \_ UTF16 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**WS \_ XML \_ UTF8 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 