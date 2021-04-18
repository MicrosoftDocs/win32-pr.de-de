---
title: Dateinamenerweiterungen
description: Dateinamenerweiterungen
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Media-Metadateien, Erweiterungen
- Windows Media-Metadateien, Dateinamen Erweiterungen
- Metadatendateien, Erweiterungen
- Metadateien, Dateinamen Erweiterungen
- Windows Media, Metafiles
- Dateinamen Erweiterungen für Windows Media-Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340853"
---
# <a name="file-name-extensions"></a><span data-ttu-id="68da4-109">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="68da4-109">File Name Extensions</span></span>

<span data-ttu-id="68da4-110">Es gibt spezielle Richtlinien für die Verwendung von Dateinamen Erweiterungen für Windows Media-Metadateien.</span><span class="sxs-lookup"><span data-stu-id="68da4-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="68da4-111">Windows Media Metadatei-Erweiterungen werden verwendet, um die verschiedenen Typen von Windows Media-Dateien zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="68da4-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="68da4-112">Eine Dateinamenerweiterung bietet einen unabhängigen Software Hersteller (Independent Software Vendor, ISV) mit Informationen zu den Renderinganforderungen einer Anwendung, die eine bestimmte Erweiterung verwendet, und ermöglicht Inhalts Entwicklern das Ausrichten allgemeiner Arten von Medien Playern.</span><span class="sxs-lookup"><span data-stu-id="68da4-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="68da4-113">Die Richtlinien für die Dateinamenerweiterung sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="68da4-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="68da4-114">Es wird empfohlen, dass der MIME-Typ einer Datei, der sich im Dateiheader befindet, für die Dateityp Identifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68da4-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="68da4-115">Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="68da4-115">File name extension</span></span> | <span data-ttu-id="68da4-116">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="68da4-116">MIME type</span></span>      | <span data-ttu-id="68da4-117">Dateiinhalte</span><span class="sxs-lookup"><span data-stu-id="68da4-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68da4-118">.wma</span><span class="sxs-lookup"><span data-stu-id="68da4-118">.wma</span></span>                | <span data-ttu-id="68da4-119">Audiodatei/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="68da4-119">audio/x-ms-wma</span></span> | <span data-ttu-id="68da4-120">Windows Media-Datei mit nur Audioinhalt.</span><span class="sxs-lookup"><span data-stu-id="68da4-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="68da4-121">Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="68da4-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="68da4-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="68da4-122">.wmv</span></span>                | <span data-ttu-id="68da4-123">Video/x-ms-WMV</span><span class="sxs-lookup"><span data-stu-id="68da4-123">video/x-ms-wmv</span></span> | <span data-ttu-id="68da4-124">Windows Media-Datei mit Audioinhalt und/oder Videoinhalt.</span><span class="sxs-lookup"><span data-stu-id="68da4-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="68da4-125">Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="68da4-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="68da4-126">.asf</span><span class="sxs-lookup"><span data-stu-id="68da4-126">.asf</span></span>                | <span data-ttu-id="68da4-127">Video/x-ms-ASF</span><span class="sxs-lookup"><span data-stu-id="68da4-127">video/x-ms-asf</span></span> | <span data-ttu-id="68da4-128">Legacy Inhalt.</span><span class="sxs-lookup"><span data-stu-id="68da4-128">Legacy content.</span></span> <span data-ttu-id="68da4-129">Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="68da4-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="68da4-130">Kann Audioinhalte und/oder Videoinhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="68da4-130">May contain audio and/or video content.</span></span> <span data-ttu-id="68da4-131">Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="68da4-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="68da4-132">WM</span><span class="sxs-lookup"><span data-stu-id="68da4-132">.wm</span></span>                 | <span data-ttu-id="68da4-133">Video/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="68da4-133">video/x-ms-wm</span></span>  | <span data-ttu-id="68da4-134">Reserviert</span><span class="sxs-lookup"><span data-stu-id="68da4-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="68da4-135">. Wachs</span><span class="sxs-lookup"><span data-stu-id="68da4-135">.wax</span></span>                | <span data-ttu-id="68da4-136">Audiodatei/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="68da4-136">audio/x-ms-wax</span></span> | <span data-ttu-id="68da4-137">Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. ASF,. WMA oder. Wax verweisen.</span><span class="sxs-lookup"><span data-stu-id="68da4-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="68da4-138">. wvx</span><span class="sxs-lookup"><span data-stu-id="68da4-138">.wvx</span></span>                | <span data-ttu-id="68da4-139">Video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="68da4-139">video/x-ms-wvx</span></span> | <span data-ttu-id="68da4-140">Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. WMA,. WMV,. wvx oder. Wax verweisen.</span><span class="sxs-lookup"><span data-stu-id="68da4-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="68da4-141">.asx</span><span class="sxs-lookup"><span data-stu-id="68da4-141">.asx</span></span>                | <span data-ttu-id="68da4-142">Video/x-ms-ASF</span><span class="sxs-lookup"><span data-stu-id="68da4-142">video/x-ms-asf</span></span> | <span data-ttu-id="68da4-143">Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. WMA,. Wax,. WMV,. wvx,. ASF oder. ASX verweisen.</span><span class="sxs-lookup"><span data-stu-id="68da4-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="68da4-144">. wmx</span><span class="sxs-lookup"><span data-stu-id="68da4-144">.wmx</span></span>                | <span data-ttu-id="68da4-145">Video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="68da4-145">video/x-ms-wvx</span></span> | <span data-ttu-id="68da4-146">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="68da4-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="68da4-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68da4-147">Remarks</span></span>

<span data-ttu-id="68da4-148">Skripterstellung und Digital Rights Management (DRM) müssen von jeder Anwendung unterstützt werden, die Windows Media-Dateien rendert.</span><span class="sxs-lookup"><span data-stu-id="68da4-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68da4-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68da4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68da4-150">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="68da4-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="68da4-151">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="68da4-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="68da4-152">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="68da4-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




