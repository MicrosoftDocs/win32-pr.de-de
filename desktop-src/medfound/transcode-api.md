---
description: In diesem Abschnitt wird beschrieben, wie Sie die transcodieren-API zum erneuten Codieren von Mediendateien verwenden. Die transcodieren-API wurde in Windows 7 eingeführt.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: Transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863943"
---
# <a name="transcode-api"></a><span data-ttu-id="9c191-104">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="9c191-104">Transcode API</span></span>

<span data-ttu-id="9c191-105">In diesem Abschnitt wird beschrieben, wie Sie die transcodieren-API zum erneuten Codieren von Mediendateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c191-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="9c191-106">Die transcodieren-API wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9c191-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="9c191-107">*Transcoding* ist die Konvertierung einer digitalen Mediendatei von einem Format in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="9c191-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="9c191-108">Die transcodieren-API ist für die Verwendung mit der [Medien Sitzung](media-session.md)konzipiert.</span><span class="sxs-lookup"><span data-stu-id="9c191-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="9c191-109">Es vereinfacht die Verwendung der Medien Sitzung für bestimmte Arten von Transcodierungs Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="9c191-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="9c191-110">CBR-Codierung (Constant Bitrate), bei der die Zielbitrate im Voraus bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9c191-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="9c191-111">Höchstens einen Audiostream und einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="9c191-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="9c191-112">Codierung von und in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="9c191-112">Encoding from and to a file.</span></span>

<span data-ttu-id="9c191-113">Die transcode-API unterstützt Folgendes nicht:</span><span class="sxs-lookup"><span data-stu-id="9c191-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="9c191-114">Variablenbitrate (VBR) oder Multipass-Codierung.</span><span class="sxs-lookup"><span data-stu-id="9c191-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="9c191-115">Mehrere Audiostreams oder mehrere Videostreams.</span><span class="sxs-lookup"><span data-stu-id="9c191-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="9c191-116">DRM-geschützter Inhalt, der nicht mit WMDRM geschützten ASF-Dateien ist.</span><span class="sxs-lookup"><span data-stu-id="9c191-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="9c191-117">Live Streaming, z. b. Live-zu-Datei-Streaming oder Live-zu-Live-Streaming.</span><span class="sxs-lookup"><span data-stu-id="9c191-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="9c191-118">Wenn Ihre Codierungs Anwendung in diese Einschränkungen passt, ist die transcodieren-API ein einfacheres Programmiermodell, als die Medien Sitzung allein zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c191-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9c191-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9c191-119">In this section</span></span>



| <span data-ttu-id="9c191-120">Thema</span><span class="sxs-lookup"><span data-stu-id="9c191-120">Topic</span></span>                                                                                          | <span data-ttu-id="9c191-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c191-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c191-122">Informationen zur transcode-API</span><span class="sxs-lookup"><span data-stu-id="9c191-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="9c191-123">Bietet eine allgemeine Übersicht über die transcodieren-API.</span><span class="sxs-lookup"><span data-stu-id="9c191-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="9c191-124">Verwenden der transcode-API</span><span class="sxs-lookup"><span data-stu-id="9c191-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="9c191-125">Beschreibt, wie eine Anwendung die transcodieren-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c191-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="9c191-126">Tutorial: Codieren einer MP4-Datei</span><span class="sxs-lookup"><span data-stu-id="9c191-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="9c191-127">Ein schrittweises Tutorial, das zeigt, wie Sie die transcodieren-API verwenden, um eine MP4-Datei zu codieren.</span><span class="sxs-lookup"><span data-stu-id="9c191-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="9c191-128">Tutorial: Codieren einer WMA-Datei</span><span class="sxs-lookup"><span data-stu-id="9c191-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="9c191-129">Zeigt, wie Sie die transcodieren-API verwenden, um eine WMA-Datei zu codieren.</span><span class="sxs-lookup"><span data-stu-id="9c191-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="9c191-130">In diesem Tutorial wird der in [Tutorial: Codieren einer MP4-Datei](tutorial--encoding-an-mp4-file-.md)gezeigte Code geändert. Sie sollten daher zuerst das Lernprogramm Lesen.</span><span class="sxs-lookup"><span data-stu-id="9c191-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9c191-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c191-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c191-132">Codierung und Dateierstellung</span><span class="sxs-lookup"><span data-stu-id="9c191-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="9c191-133">Media Foundation: Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="9c191-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="9c191-134">Übersicht über die Codierung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c191-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




