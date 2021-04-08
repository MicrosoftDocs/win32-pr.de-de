---
title: Metadatenerweiterungs-Richtlinien
description: Metadatenerweiterungs-Richtlinien
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
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
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037536"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="c0f7c-109">Metadatenerweiterungs-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c0f7c-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="c0f7c-110">Eine Dateinamenerweiterung bietet einen unabhängigen Softwarehersteller (Independent Software Vendor, ISV) mit Informationen zu den Renderinganforderungen einer Anwendung, die die Erweiterung verwendet, und ermöglicht Inhalts Entwicklern, allgemeine Typen von Playern als Ziel festzustellen.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="c0f7c-111">Windows Media Metadatei-Erweiterungen werden verwendet, um das Format der Windows Media-Dateien zu identifizieren, auf die eine Metadatei verweist.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="c0f7c-112">Windows Media-Metadatendateien mit den Erweiterungen ". wax", ". wvx" oder ". asx" verweisen auf die Dateien mit den Erweiterungen. WMA,. WMV und.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="c0f7c-113">Alle Metadatendateien, unabhängig von der verwendeten Dateinamenerweiterung, haben das Element " **ASX** Element" am Anfang der Datei mit dem angegebenen **Versions** Attribut.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="c0f7c-114">In der folgenden Tabelle werden die Medien Dateitypen angezeigt, auf die von den einzelnen Metadatendatei-Dateinamen Erweiterungen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="c0f7c-115">In den Spalten werden die Namen Erweiterungen für Mediendateien aufgelistet, die Metadatendatei-Erweiterungen der Zeilen Liste.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="c0f7c-116">Ein X in einer Spalte gibt einen Medien Dateityp an, auf den von einer bestimmten Dateinamenerweiterung für Metadatendateien verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0f7c-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="c0f7c-117">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="c0f7c-117">Extension</span></span> | <span data-ttu-id="c0f7c-118">.asf</span><span class="sxs-lookup"><span data-stu-id="c0f7c-118">.asf</span></span> | <span data-ttu-id="c0f7c-119">.wma</span><span class="sxs-lookup"><span data-stu-id="c0f7c-119">.wma</span></span> | <span data-ttu-id="c0f7c-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="c0f7c-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="c0f7c-121">. wvx</span><span class="sxs-lookup"><span data-stu-id="c0f7c-121">.wvx</span></span>      | <span data-ttu-id="c0f7c-122">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-122">X</span></span>    | <span data-ttu-id="c0f7c-123">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-123">X</span></span>    | <span data-ttu-id="c0f7c-124">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-124">X</span></span>    |
| <span data-ttu-id="c0f7c-125">. Wachs</span><span class="sxs-lookup"><span data-stu-id="c0f7c-125">.wax</span></span>      | <span data-ttu-id="c0f7c-126">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-126">X</span></span>    | <span data-ttu-id="c0f7c-127">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-127">X</span></span>    |      |
| <span data-ttu-id="c0f7c-128">.asx</span><span class="sxs-lookup"><span data-stu-id="c0f7c-128">.asx</span></span>      | <span data-ttu-id="c0f7c-129">X</span><span class="sxs-lookup"><span data-stu-id="c0f7c-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="c0f7c-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0f7c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0f7c-131">**Dateinamenerweiterungen**</span><span class="sxs-lookup"><span data-stu-id="c0f7c-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="c0f7c-132">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="c0f7c-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="c0f7c-133">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="c0f7c-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




