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
# <a name="xml-writer"></a><span data-ttu-id="8ed42-107">XML-Writer</span><span class="sxs-lookup"><span data-stu-id="8ed42-107">XML Writer</span></span>

<span data-ttu-id="8ed42-108">Der XML-Writer ist eine API zum Ausgeben von XML.</span><span class="sxs-lookup"><span data-stu-id="8ed42-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="8ed42-109">Im Kern schreibt ein XML-Writer jeweils einen [XML-Knoten](xml-node.md) . es gibt jedoch zusätzliche hilfsapis, mit denen das Schreiben einer Sequenz von Knoten vereinfacht wird.</span><span class="sxs-lookup"><span data-stu-id="8ed42-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="8ed42-110">Die folgenden Arten von Writer-Ausgaben werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8ed42-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="8ed42-111">**Ein Puffer im Arbeitsspeicher codierter Bytes**</span><span class="sxs-lookup"><span data-stu-id="8ed42-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="8ed42-112">**Ein Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="8ed42-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="8ed42-113">Ein [XML-Puffer](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="8ed42-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="8ed42-114">Die folgenden Rückrufe werden mit dem XML-Writer verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ed42-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="8ed42-115">**WS- \_ dynamischer \_ Zeichen folgen \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8ed42-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="8ed42-116">**WS- \_ Pull- \_ Bytes- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8ed42-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="8ed42-117">**WS- \_ Push- \_ Bytes- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8ed42-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="8ed42-118">**WS- \_ Schreib \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8ed42-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="8ed42-119">Die folgenden Enumerationen werden mit dem XML-Writer verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ed42-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="8ed42-120">**WS-Zeichen \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="8ed42-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="8ed42-121">**WS \_ XML \_ Writer \_ - \_ Codierungstyp**</span><span class="sxs-lookup"><span data-stu-id="8ed42-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="8ed42-122">**Ausgabe des WS \_ XML \_ Writer- \_ Ausgabe \_ Typs**</span><span class="sxs-lookup"><span data-stu-id="8ed42-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="8ed42-123">**WS \_ XML \_ Writer- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="8ed42-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="8ed42-124">Die folgenden Funktionen werden mit dem XML-Writer verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ed42-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="8ed42-125">**Wscopynode**</span><span class="sxs-lookup"><span data-stu-id="8ed42-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="8ed42-126">**Wscreatewriter**</span><span class="sxs-lookup"><span data-stu-id="8ed42-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="8ed42-127">**Wsflushwriter**</span><span class="sxs-lookup"><span data-stu-id="8ed42-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="8ed42-128">**Wsfrewriter**</span><span class="sxs-lookup"><span data-stu-id="8ed42-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="8ed42-129">**Wsgetprefixfromnamespace**</span><span class="sxs-lookup"><span data-stu-id="8ed42-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="8ed42-130">**Wsgetschreiterposition**</span><span class="sxs-lookup"><span data-stu-id="8ed42-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="8ed42-131">**Wsgetschreiterproperty**</span><span class="sxs-lookup"><span data-stu-id="8ed42-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="8ed42-132">**Wsmovewriter**</span><span class="sxs-lookup"><span data-stu-id="8ed42-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="8ed42-133">**Wspullbytes**</span><span class="sxs-lookup"><span data-stu-id="8ed42-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="8ed42-134">**Wspushbytes**</span><span class="sxs-lookup"><span data-stu-id="8ed42-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="8ed42-135">**Wssetoutput**</span><span class="sxs-lookup"><span data-stu-id="8ed42-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="8ed42-136">**Wssetoutputtbuffer**</span><span class="sxs-lookup"><span data-stu-id="8ed42-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="8ed42-137">**Wssetschreiterposition**</span><span class="sxs-lookup"><span data-stu-id="8ed42-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="8ed42-138">**Wsschreitearray**</span><span class="sxs-lookup"><span data-stu-id="8ed42-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="8ed42-139">**Wsschreitebytes**</span><span class="sxs-lookup"><span data-stu-id="8ed42-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="8ed42-140">**Wswrite techars**</span><span class="sxs-lookup"><span data-stu-id="8ed42-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="8ed42-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="8ed42-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="8ed42-142">**Wsschreiteendattribute**</span><span class="sxs-lookup"><span data-stu-id="8ed42-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="8ed42-143">**Wsschreiteendcdata**</span><span class="sxs-lookup"><span data-stu-id="8ed42-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="8ed42-144">**Wsschreiteendelta-Element**</span><span class="sxs-lookup"><span data-stu-id="8ed42-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="8ed42-145">**Wsschreitenode**</span><span class="sxs-lookup"><span data-stu-id="8ed42-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="8ed42-146">**Wsschreitequalifiedname**</span><span class="sxs-lookup"><span data-stu-id="8ed42-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="8ed42-147">**Wsschreitestartattribute**</span><span class="sxs-lookup"><span data-stu-id="8ed42-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="8ed42-148">**Wsschreitestartcdata**</span><span class="sxs-lookup"><span data-stu-id="8ed42-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="8ed42-149">**Wsschreitestartelements**</span><span class="sxs-lookup"><span data-stu-id="8ed42-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="8ed42-150">**Wsschreitetext**</span><span class="sxs-lookup"><span data-stu-id="8ed42-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="8ed42-151">**Wsschreitevalue**</span><span class="sxs-lookup"><span data-stu-id="8ed42-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="8ed42-152">**Wsschreitexmlnsattribute**</span><span class="sxs-lookup"><span data-stu-id="8ed42-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="8ed42-153">Der folgende Handle wird mit dem XML-Writer verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ed42-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="8ed42-154">WS- \_ XML- \_ Writer</span><span class="sxs-lookup"><span data-stu-id="8ed42-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="8ed42-155">Die folgenden Strukturen werden mit dem XML-Writer verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ed42-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="8ed42-156">**\_binäre WS XML \_ Writer- \_ \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="8ed42-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="8ed42-157">**Ausgabe des WS \_ XML \_ Writer- \_ Puffers \_**</span><span class="sxs-lookup"><span data-stu-id="8ed42-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="8ed42-158">**WS- \_ XML- \_ Writer- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="8ed42-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="8ed42-159">**WS \_ XML \_ Writer- \_ MTOM- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="8ed42-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="8ed42-160">**Ausgabe des WS \_ XML \_ Writer \_**</span><span class="sxs-lookup"><span data-stu-id="8ed42-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="8ed42-161">**Eigenschaften von WS \_ XML \_ Writer \_**</span><span class="sxs-lookup"><span data-stu-id="8ed42-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="8ed42-162">**WS \_ XML \_ Writer ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="8ed42-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="8ed42-163">**Ausgabe des WS \_ XML \_ Writer- \_ Streams \_**</span><span class="sxs-lookup"><span data-stu-id="8ed42-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="8ed42-164">**WS \_ XML \_ Writer- \_ Text \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="8ed42-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




