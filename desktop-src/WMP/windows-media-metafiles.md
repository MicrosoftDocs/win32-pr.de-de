---
title: Windows Media-Metadateien
description: Windows Media-Metadateien
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
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
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310067"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="6bbca-111">Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="6bbca-111">Windows Media Metafiles</span></span>

<span data-ttu-id="6bbca-112">Diese Referenz dokumentiert Windows Media-Metadateien, die die Dateinamen Erweiterungen ". wax", ". wvx", ". wmx" und ". asx" verwenden.</span><span class="sxs-lookup"><span data-stu-id="6bbca-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="6bbca-113">Es enthält Abschnitte für die Übersicht und den Programmier Leit Faden sowie einen vollständigen Referenz Abschnitt zu metadateielementtags, deren Attributen und Werten sowie spezielle Bedingungen im Zusammenhang mit den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="6bbca-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="6bbca-114">Eine Metadatei ist eine Datei, die Informationen zu anderen Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="6bbca-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="6bbca-115">Eine Metadatei kann verwendet werden, um eine Gruppe von Medien Inhalts Dateien aufzulisten, die in der richtigen Reihenfolge wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bbca-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="6bbca-116">Windows Media Metadatei-Wiedergabelisten, die in diesem Referenzdokument als Wiedergabelisten bezeichnet werden, sind eines der leistungsstärksten Features von Microsoft Windows Media-Technologien.</span><span class="sxs-lookup"><span data-stu-id="6bbca-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="6bbca-117">Mit Wiedergabelisten können Sie Ihre Medieninhalte Steuern und anpassen.</span><span class="sxs-lookup"><span data-stu-id="6bbca-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="6bbca-118">Beispielsweise können Sie mit Wiedergabelisten Inhalte so planen, dass Sie nacheinander wiedergegeben werden, oder Sie können Werbung oder besondere interessante Clips in eine Präsentation einfügen.</span><span class="sxs-lookup"><span data-stu-id="6bbca-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="6bbca-119">Ein weiterer Vorteil von Wiedergabelisten besteht darin, dass statt eines Streams, beenden, Starten des nächsten Streams und anschließendes warten darauf, dass die Pufferung abgeschlossen wird, Windows Media Services und Windows Media Player zusammenarbeiten, um die Clips nacheinander zu wiedergeben. dabei wird nur eine minimale Pufferzeit oder eine Unterbrechung zwischen Ihnen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6bbca-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="6bbca-120">Windows Media-Technologien und andere Internet Produkte bieten Ihnen die Tools, mit denen Sie Benutzer demografiken verstehen und eine Übertragung oder Nachricht für einzelne Benutzer dynamisch anpassen können.</span><span class="sxs-lookup"><span data-stu-id="6bbca-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="6bbca-121">Dieser Verweis ist in die folgenden Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="6bbca-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="6bbca-122">`Section`</span><span class="sxs-lookup"><span data-stu-id="6bbca-122">Section</span></span>                                                                  | <span data-ttu-id="6bbca-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bbca-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bbca-124">Informationen zu Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="6bbca-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="6bbca-125">Führt Windows Media-Metadatei-Elemente ein und erläutert ihren Zweck.</span><span class="sxs-lookup"><span data-stu-id="6bbca-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="6bbca-126">Leitfaden für Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="6bbca-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="6bbca-127">Erläutert die Schritte, die zum Erstellen von Metadateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6bbca-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="6bbca-128">Beispiele veranschaulichen, wie Element Tags für bestimmte Aufgaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bbca-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="6bbca-129">Referenz zu Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="6bbca-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="6bbca-130">Erläutert ausführlich alle Metadatei-Elemente, ihre Attribute und Werte sowie spezielle, im Zusammenhang stehende Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="6bbca-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="6bbca-131">Erläutert metadatendateiname-Erweiterungen und ihre ordnungsgemäße Verwendung.</span><span class="sxs-lookup"><span data-stu-id="6bbca-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6bbca-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6bbca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bbca-133">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="6bbca-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




