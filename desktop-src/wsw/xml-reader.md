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
# <a name="xml-reader"></a><span data-ttu-id="89f01-107">XML-Reader</span><span class="sxs-lookup"><span data-stu-id="89f01-107">XML Reader</span></span>

<span data-ttu-id="89f01-108">Der XML-Reader ist ein Cursor über einer Eingabe Quelle von XML.</span><span class="sxs-lookup"><span data-stu-id="89f01-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="89f01-109">Im Kern liest ein XML-Reader jeweils einen [XML-Knoten](xml-node.md) . es gibt jedoch zusätzliche hilfsapis, mit denen das Lesen einer Sequenz von Knoten vereinfacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="89f01-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="89f01-110">Die folgenden Arten von Leser Eingaben werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="89f01-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="89f01-111">**Ein Puffer im Arbeitsspeicher codierter Bytes**</span><span class="sxs-lookup"><span data-stu-id="89f01-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="89f01-112">**Ein Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="89f01-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="89f01-113">Ein [XML-Puffer](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="89f01-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="89f01-114">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="89f01-114">Security</span></span>

<span data-ttu-id="89f01-115">Der Reader überprüft, ob die Attribute, die für ein Element vorhanden sind, eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="89f01-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="89f01-116">Die Zeit, die zum Ausführen dieser Überprüfung erforderlich ist, ist eine Funktion der Anzahl von Attributen für das Element, die so groß wie die Attribute "Max" der [**WS \_ XML \_ Reader- \_ Eigenschaft \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)sein kann.</span><span class="sxs-lookup"><span data-stu-id="89f01-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="89f01-117">Daher kann es vorkommen, dass große Dokumente verarbeitet werden, wenn die **\_ \_ \_ Eigenschaft \_ Max \_ Attribute der WS XML-Reader-Eigenschaft** auf einen großen Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="89f01-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="89f01-118">Der Reader ordnet Namespaces Präfixe für jedes Element und jedes Attribut zu.</span><span class="sxs-lookup"><span data-stu-id="89f01-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="89f01-119">Die Zeit, die zum Ausführen dieser Zuordnung erforderlich ist, ist eine Funktion der Anzahl von xmlns-Attributen im Bereich, die möglicherweise so groß wie die maximale Anzahl von [**\_ \_ \_ \_ \_ Namespaces der WS XML-Reader-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)ist</span><span class="sxs-lookup"><span data-stu-id="89f01-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="89f01-120">Daher kann die Verarbeitung großer Dokumente, wenn diese Eigenschaft auf einen hohen Wert festgelegt ist, eine Gelegenheit für einen Denial-of-Service-Angriff darstellen.</span><span class="sxs-lookup"><span data-stu-id="89f01-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="89f01-121">Während der Reader sicherstellt, dass das Dokument der grammatikalen Spezifikation von XML folgt und die zugehörigen Aspekte in den angegebenen Kontingenten liegen, muss der Inhalt des Dokuments weiterhin als nicht vertrauenswürdig eingestuft werden, wenn er von einer nicht vertrauenswürdigen Quelle stammt.</span><span class="sxs-lookup"><span data-stu-id="89f01-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="89f01-122">Benutzer des Readers sollten alle Element-und Attributnamen und Namespaces mithilfe von [**wslesetostartelement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**wsfindattribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)oder durch Manuelles Überprüfen von [**Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="89f01-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="89f01-123">Einige andere zu berücksichtigende Situationen sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="89f01-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="89f01-124">Erwartete Elemente fehlen möglicherweise.</span><span class="sxs-lookup"><span data-stu-id="89f01-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="89f01-125">Unerwartete Elemente werden möglicherweise angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89f01-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="89f01-126">Möglicherweise fehlen Attribute.</span><span class="sxs-lookup"><span data-stu-id="89f01-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="89f01-127">Unerwartete Attribute können angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89f01-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="89f01-128">Elemente können als leere Elemente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89f01-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="89f01-129">Leerräume werden möglicherweise an unerwarteten Stellen angezeigt</span><span class="sxs-lookup"><span data-stu-id="89f01-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="89f01-130">Benutzer des Readers sollten keinen Speicher basierend auf den aus dem Dokument gelesenen Werten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="89f01-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="89f01-131">Sehen Sie sich beispielsweise das folgende XML-Dokument an:</span><span class="sxs-lookup"><span data-stu-id="89f01-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="89f01-132">Die Zuweisung eines Array basierten Soley in der Annahme, dass eine bestimmte Anzahl von Elementen befolgt wird, wäre ein potenzieller Angriffsvektor.</span><span class="sxs-lookup"><span data-stu-id="89f01-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="89f01-133">Der Benutzer des Readers sollte in diesem Fall stattdessen den Arbeitsspeicher inkrementell zuweisen, wenn die Elemente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89f01-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="89f01-134">Der XML-Reader unterstützt DTD nicht.</span><span class="sxs-lookup"><span data-stu-id="89f01-134">XML reader does not support DTD.</span></span> <span data-ttu-id="89f01-135">Der Benutzer des Readers muss sich nicht mit der DTD-Überprüfung befassen.</span><span class="sxs-lookup"><span data-stu-id="89f01-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="89f01-136">Der folgende Rückruf wird bei XML-Lesern verwendet:</span><span class="sxs-lookup"><span data-stu-id="89f01-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="89f01-137">**WS- \_ Lese \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="89f01-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="89f01-138">Die folgenden Enumerationen werden mit XML-Lesern verwendet:</span><span class="sxs-lookup"><span data-stu-id="89f01-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="89f01-139">**WS- \_ XML- \_ \_ \_ lesecodierungstyp**</span><span class="sxs-lookup"><span data-stu-id="89f01-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="89f01-140">**\_ \_ \_ Eingabe \_ Typen des WS XML-Readers**</span><span class="sxs-lookup"><span data-stu-id="89f01-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="89f01-141">**Eigenschaften-ID der WS XML- \_ \_ Reader \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89f01-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="89f01-142">Die folgenden Funktionen werden mit XML-Lesern verwendet:</span><span class="sxs-lookup"><span data-stu-id="89f01-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="89f01-143">**Wscreatereader**</span><span class="sxs-lookup"><span data-stu-id="89f01-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="89f01-144">**Wsfillreader**</span><span class="sxs-lookup"><span data-stu-id="89f01-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="89f01-145">**Wsfindattribute**</span><span class="sxs-lookup"><span data-stu-id="89f01-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="89f01-146">**Wsfreereader**</span><span class="sxs-lookup"><span data-stu-id="89f01-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="89f01-147">**Wsgetnamespacefromprefix**</span><span class="sxs-lookup"><span data-stu-id="89f01-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="89f01-148">**Wsgetreadernode**</span><span class="sxs-lookup"><span data-stu-id="89f01-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="89f01-149">**Wsgetreaderposition**</span><span class="sxs-lookup"><span data-stu-id="89f01-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="89f01-150">**Wsgetreaderproperty**</span><span class="sxs-lookup"><span data-stu-id="89f01-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="89f01-151">**Wsgetxmlattribute**</span><span class="sxs-lookup"><span data-stu-id="89f01-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="89f01-152">**Wsmovereader**</span><span class="sxs-lookup"><span data-stu-id="89f01-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="89f01-153">**Wslesarray**</span><span class="sxs-lookup"><span data-stu-id="89f01-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="89f01-154">**Wslebytes**</span><span class="sxs-lookup"><span data-stu-id="89f01-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="89f01-155">**Wsleserchars**</span><span class="sxs-lookup"><span data-stu-id="89f01-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="89f01-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="89f01-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="89f01-157">**Wsumdattribute**</span><span class="sxs-lookup"><span data-stu-id="89f01-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="89f01-158">**Wsleserumdelta**</span><span class="sxs-lookup"><span data-stu-id="89f01-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="89f01-159">**Wsread Node**</span><span class="sxs-lookup"><span data-stu-id="89f01-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="89f01-160">**Wsleserqualifiedname**</span><span class="sxs-lookup"><span data-stu-id="89f01-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="89f01-161">**Wsleserstartattribute**</span><span class="sxs-lookup"><span data-stu-id="89f01-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="89f01-162">**Wsleserstartelements**</span><span class="sxs-lookup"><span data-stu-id="89f01-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="89f01-163">**Wsumstartelements**</span><span class="sxs-lookup"><span data-stu-id="89f01-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="89f01-164">**Wsread Value**</span><span class="sxs-lookup"><span data-stu-id="89f01-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="89f01-165">**Wssetinput**</span><span class="sxs-lookup"><span data-stu-id="89f01-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="89f01-166">**Wssetinputstobuffer**</span><span class="sxs-lookup"><span data-stu-id="89f01-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="89f01-167">**Wssetreaderposition**</span><span class="sxs-lookup"><span data-stu-id="89f01-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="89f01-168">**Wsskipnode**</span><span class="sxs-lookup"><span data-stu-id="89f01-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="89f01-169">Das folgende Handle wird bei XML-Lesern verwendet:</span><span class="sxs-lookup"><span data-stu-id="89f01-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="89f01-170">WS- \_ XML- \_ Reader</span><span class="sxs-lookup"><span data-stu-id="89f01-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="89f01-171">Die folgenden Strukturen werden mit XML-Lesern verwendet:</span><span class="sxs-lookup"><span data-stu-id="89f01-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="89f01-172">**\_ \_ \_ Binär \_ Codierung des WS XML-Readers**</span><span class="sxs-lookup"><span data-stu-id="89f01-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="89f01-173">**WS- \_ XML- \_ Reader- \_ Puffer \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="89f01-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="89f01-174">**WS- \_ XML- \_ Reader- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="89f01-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="89f01-175">**WS- \_ XML- \_ Reader- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="89f01-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="89f01-176">**WS- \_ XML- \_ Reader- \_ MTOM- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="89f01-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="89f01-177">**Eigenschaften des WS- \_ XML- \_ Readers \_**</span><span class="sxs-lookup"><span data-stu-id="89f01-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="89f01-178">**WS \_ XML \_ Reader ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="89f01-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="89f01-179">**WS \_ XML \_ Reader \_ Stream- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="89f01-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="89f01-180">**WS- \_ XML- \_ Reader- \_ Text \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="89f01-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




