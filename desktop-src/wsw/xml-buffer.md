---
title: XML-Puffer
description: Ein XML-Puffer stellt einen effizienten Speicher internen Speicher für beliebige XML-Daten bereit.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- XML-Puffer-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949233"
---
# <a name="xml-buffer"></a><span data-ttu-id="fc092-106">XML-Puffer</span><span class="sxs-lookup"><span data-stu-id="fc092-106">XML Buffer</span></span>

<span data-ttu-id="fc092-107">Ein XML-Puffer stellt einen effizienten Speicher internen Speicher für beliebige XML-Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="fc092-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="fc092-108">Verwenden Sie zum Lesen von Daten aus einem XML-Puffer einen [XML-Reader](xml-reader.md) , und nennen Sie [**wssetinputesbuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) mit dem XML-Puffer.</span><span class="sxs-lookup"><span data-stu-id="fc092-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="fc092-109">Der Reader wird am Anfang des Dokuments positioniert.</span><span class="sxs-lookup"><span data-stu-id="fc092-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="fc092-110">Verwenden Sie zum Einfügen von Daten in einen Puffer einen [XML-Writer](xml-writer.md) , und nennen Sie [**wssetoutputstobuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) mit dem XML-Puffer.</span><span class="sxs-lookup"><span data-stu-id="fc092-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="fc092-111">Der Writer wird am Ende des Dokuments positioniert.</span><span class="sxs-lookup"><span data-stu-id="fc092-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="fc092-112">Nachdem ein Reader auf einen XML-Puffer festgelegt wurde, kann er zusätzlich zu allen XML-Reader-APIs [**verwendet werden,**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) um den Reader durch das Dokument zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="fc092-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="fc092-113">[**Wsgetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) und [**wssetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) können auch verwendet werden, um eine Position im Dokument aufzuzeichnen und zu einem späteren Zeitpunkt zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="fc092-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="fc092-114">Nachdem ein Writer auf einen XML-Puffer festgelegt wurde, kann [**wsmovewriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) zusätzlich zu allen XML-Writer-APIs verwendet werden, um im Writer durch das Dokument zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="fc092-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="fc092-115">[**Wsgetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) und [**wssetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) können auch verwendet werden, um eine Position im Dokument aufzuzeichnen und zu einem späteren Zeitpunkt zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="fc092-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="fc092-116">Der Writer fügt immer Daten vor dem Knoten ein, auf dem er positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="fc092-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="fc092-117">Knoten können aus dem XML-Puffer gelöscht werden, indem Sie die Position des Knotens mithilfe von [**wsgetreaderposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) oder [**wsgetschreiterposition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) abrufen und dann [**wsremovenode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) mit dieser Position aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc092-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="fc092-118">Bei-Elementen wird dadurch das-Element, alle seine untergeordneten Elemente einschließlich des entsprechenden End-Elements gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fc092-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="fc092-119">Eine Position wird durch die Position des Werts der [**WS- \_ XML- \_ Knoten \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fc092-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="fc092-120">Positionen sind spezifisch für einen bestimmten XML-Puffer und sind nur gültig, solange der XML-Puffer gültig ist.</span><span class="sxs-lookup"><span data-stu-id="fc092-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="fc092-121">Die folgenden Enumerationen werden mit XML-Puffern verwendet:</span><span class="sxs-lookup"><span data-stu-id="fc092-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="fc092-122">**WS- \_ Verschiebung \_ zu**</span><span class="sxs-lookup"><span data-stu-id="fc092-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="fc092-123">**Eigenschaften-ID der WS XML- \_ \_ Puffer \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc092-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="fc092-124">Die folgenden Funktionen werden für XML-Puffer verwendet:</span><span class="sxs-lookup"><span data-stu-id="fc092-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="fc092-125">**Wscreatexmlbuffer**</span><span class="sxs-lookup"><span data-stu-id="fc092-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="fc092-126">**Wsremovenode**</span><span class="sxs-lookup"><span data-stu-id="fc092-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="fc092-127">Das folgende Handle wird für XML-Puffer verwendet:</span><span class="sxs-lookup"><span data-stu-id="fc092-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="fc092-128">WS- \_ XML- \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="fc092-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="fc092-129">Die folgenden Strukturen werden mit XML-Puffern verwendet:</span><span class="sxs-lookup"><span data-stu-id="fc092-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="fc092-130">**WS \_ XML- \_ Puffer ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="fc092-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="fc092-131">**WS- \_ XML- \_ Knoten \_ Position**</span><span class="sxs-lookup"><span data-stu-id="fc092-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




