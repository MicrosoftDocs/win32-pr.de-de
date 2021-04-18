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
# <a name="xml-node"></a><span data-ttu-id="5be4a-107">XML-Knoten</span><span class="sxs-lookup"><span data-stu-id="5be4a-107">XML Node</span></span>

<span data-ttu-id="5be4a-108">Ein XML-Knoten stellt ein einzelnes XML-Element dar, z. b. ein Start Element und seine Attribute, ein Endelement, Text oder einen "typisierten" Text Inhalt, z. b. eine ganze Zahl oder ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="5be4a-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="5be4a-109">Die Daten in einem Knoten variieren je nach dem [**Typ des WS- \_ XML- \_ Knotens \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="5be4a-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="5be4a-110">Im folgenden finden Sie ein Beispiel für ein Codierungs spezifisches XML-Dokument, das mit codierten unabhängigen Strukturen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5be4a-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

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

<span data-ttu-id="5be4a-111">Die folgenden Enumerationen werden mit XML-Knoten verwendet:</span><span class="sxs-lookup"><span data-stu-id="5be4a-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="5be4a-112">**WS \_ - \_ Werttyp**</span><span class="sxs-lookup"><span data-stu-id="5be4a-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="5be4a-113">**WS- \_ XML- \_ \_ Knotentyp**</span><span class="sxs-lookup"><span data-stu-id="5be4a-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="5be4a-114">**WS- \_ XML- \_ \_ Texttyp**</span><span class="sxs-lookup"><span data-stu-id="5be4a-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="5be4a-115">Die folgenden Funktionen werden mit XML-Knoten verwendet:</span><span class="sxs-lookup"><span data-stu-id="5be4a-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="5be4a-116">**Wstrimxmlwhitespace**</span><span class="sxs-lookup"><span data-stu-id="5be4a-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="5be4a-117">**Wsverifyxmlncname**</span><span class="sxs-lookup"><span data-stu-id="5be4a-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="5be4a-118">**Wsxmlstringequals**</span><span class="sxs-lookup"><span data-stu-id="5be4a-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="5be4a-119">Die folgenden Makros werden mit XML-Knoten verwendet:</span><span class="sxs-lookup"><span data-stu-id="5be4a-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="5be4a-120">**WS- \_ XML- \_ Zeichen folgen \_ \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="5be4a-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="5be4a-121">[**WS- \_ XML- \_ Zeichenfolge \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5be4a-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="5be4a-122">**WS- \_ XML- \_ Zeichen folgen \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="5be4a-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="5be4a-123">Die folgenden Strukturen werden mit XML-Knoten verwendet:</span><span class="sxs-lookup"><span data-stu-id="5be4a-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="5be4a-124">**WS- \_ XML- \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="5be4a-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="5be4a-125">**WS- \_ XML- \_ Base64- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="5be4a-126">**\_ \_ boolescher Text von WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="5be4a-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="5be4a-127">**WS- \_ XML- \_ Kommentar \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="5be4a-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="5be4a-128">**WS \_ XML- \_ DateTime- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="5be4a-129">**WS \_ XML- \_ Dezimal \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="5be4a-130">**WS \_ XML- \_ Wörterbuch**</span><span class="sxs-lookup"><span data-stu-id="5be4a-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="5be4a-131">**\_ \_ doppelter \_ Text in WS XML**</span><span class="sxs-lookup"><span data-stu-id="5be4a-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="5be4a-132">**WS- \_ XML- \_ Element \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="5be4a-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="5be4a-133">**WS- \_ XML- \_ float- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="5be4a-134">**WS- \_ XML- \_ GUID- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="5be4a-135">**WS \_ XML \_ Int32 \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="5be4a-136">**WS \_ XML \_ Int64 \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="5be4a-137">**WS- \_ XML- \_ Listen \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="5be4a-138">**WS- \_ XML- \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="5be4a-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="5be4a-139">**WS- \_ XML- \_ QName**</span><span class="sxs-lookup"><span data-stu-id="5be4a-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="5be4a-140">**WS- \_ XML- \_ QName- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="5be4a-141">**WS \_ XML- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5be4a-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="5be4a-142">**WS- \_ XML- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="5be4a-143">**WS \_ XML- \_ Text \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="5be4a-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="5be4a-144">**WS \_ XML \_ TimeSpan- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="5be4a-145">**WS \_ XML \_ UINT64 \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="5be4a-146">**eindeutiger WS \_ XML- \_ ID- \_ \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="5be4a-147">**WS \_ XML \_ UTF16 \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="5be4a-148">**WS- \_ XML- \_ UTF8- \_ Text**</span><span class="sxs-lookup"><span data-stu-id="5be4a-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 