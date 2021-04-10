---
title: Leitfaden für Windows Media-Metadateien
description: Leitfaden für Windows Media-Metadateien
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Windows Media-Metadateien, Informationen zu
- Windows Media Player, Metafiles
- Windows Media Player, Windows Media-Metadateien
- Metadatendateien, Informationen zu
- Windows Media, Metafiles
- Windows Media Metadatei-Wiedergabelisten, Informationen zu
- Wiedergabelisten, Informationen
- Metadatei-Wiedergabelisten, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948026"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="8186f-111">Leitfaden für Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="8186f-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="8186f-112">Eine Windows Media-Metadatei kann so einfach oder komplex sein, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="8186f-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="8186f-113">Die grundlegendste Windows Media-Metadatendatei enthält nur die Uniform Resource Locator (URL) einiger multimediakhalte auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="8186f-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="8186f-114">Der Client, Windows Media Player, analysiert diese Informationen und öffnet dann die in der Windows Media-Metadatendatei definierte Mediendatei oder den Stream.</span><span class="sxs-lookup"><span data-stu-id="8186f-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="8186f-115">Eine komplexe Metadatei kann mehrere Dateien oder Streams enthalten, die in einer Wiedergabeliste angeordnet sind, Anweisungen zum Abspielen der Dateien oder Streams, Text-und Grafikelemente, wie z. b. Titel, Autor und Urheberrechts Text, personalisiertes einfügevorschub in einen Livestream, Links, die Elementen in der Windows Media Player-Schnittstelle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8186f-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="8186f-116">Die folgenden Abschnitte enthalten ausführliche Informationen zum Erstellen und Verwenden von Windows Media-metadateiwiedergabe Listen.</span><span class="sxs-lookup"><span data-stu-id="8186f-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="8186f-117">`Section`</span><span class="sxs-lookup"><span data-stu-id="8186f-117">Section</span></span>                                                            | <span data-ttu-id="8186f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8186f-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8186f-119">Typen von Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="8186f-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="8186f-120">Listet die verfügbaren Dateinamen Erweiterungen auf.</span><span class="sxs-lookup"><span data-stu-id="8186f-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="8186f-121">Erstellen von Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="8186f-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="8186f-122">Hier wird beschrieben, wie Windows Media Metadatei-Wiedergabelisten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8186f-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="8186f-123">Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="8186f-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="8186f-124">Beschreibt die Verwendung, Skripterstellung, Metadaten und Verarbeitung von Metadatei-Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="8186f-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="8186f-125">Metadatenerweiterungs-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8186f-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="8186f-126">Beschreibt die bevorzugte Verwendung von Dateinamen Erweiterungen für das Streamen von Mediendateien.</span><span class="sxs-lookup"><span data-stu-id="8186f-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="8186f-127">Rangfolge</span><span class="sxs-lookup"><span data-stu-id="8186f-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="8186f-128">Beschreibt, wie Metadatei-Wiedergabelisten Elemente andere Metadatei-Wiedergabelisten Elemente überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8186f-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8186f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8186f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8186f-130">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="8186f-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8186f-131">**Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="8186f-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




