---
title: Funktionsweise von Windows Media-Download Paketen (veraltet)
description: Funktionsweise von Windows Media-Download Paketen (veraltet)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Windows Media Download Packages, Informationen zu
- Windows Media Download Packages, Funktionsweise von Paketen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100679"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="a5207-109">Funktionsweise von Windows Media-Download Paketen (veraltet)</span><span class="sxs-lookup"><span data-stu-id="a5207-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="a5207-110">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a5207-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="a5207-111">Ein Windows Media-Download Paket wird von einer Website gestartet, wenn ein Benutzer auf einen Link in einem Webbrowser klickt (z. b. Microsoft Internet Explorer).</span><span class="sxs-lookup"><span data-stu-id="a5207-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="a5207-112">Mit dieser Aktion wird Windows Media Player geöffnet. Anschließend wird das Windows Media-Download Paket auf der Festplatte des Benutzers in einem Standardordner heruntergeladen und entpackt.</span><span class="sxs-lookup"><span data-stu-id="a5207-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="a5207-113">Nachdem die Dateien aus dem Windows Media-Download Paket extrahiert wurden, wird in Windows Media Player eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" unter den gepackten Dateien gesucht.</span><span class="sxs-lookup"><span data-stu-id="a5207-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="a5207-114">Wenn ein solcher gefunden wird, erstellt der Spieler eine Wiedergabeliste basierend auf der enthaltenen Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="a5207-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="a5207-115">Dateien, die Multimedia-Inhalte enthalten, werden dann der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a5207-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="a5207-116">Windows Media Player sucht auch nach einem **Skin** -Element in der Metadatei.</span><span class="sxs-lookup"><span data-stu-id="a5207-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="a5207-117">Wenn das **Skin** -Element einen Verweis auf eine Rahmen Datei mit der Dateinamenerweiterung ". WMZ" enthält, lädt der Spieler den Rahmen in den Bereich " **jetzt Wiedergabe** ".</span><span class="sxs-lookup"><span data-stu-id="a5207-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="a5207-118">Der Player startet dann den Inhalt, der im Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5207-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="a5207-119">Das folgende Diagramm zeigt, wie Inhalte in einer Windows Media-Download Datei verpackt, auf einer Website veröffentlicht, heruntergeladen und auf einem Client Computer mit Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="a5207-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![wie eine Windows Media-Downloaddatei abgerufen und wiedergegeben wird.](images/wmd-image.png) <span data-ttu-id="a5207-121">Windows Media-Download</span><span class="sxs-lookup"><span data-stu-id="a5207-121">Windows Media Download</span></span>

<span data-ttu-id="a5207-122">In der folgenden Tabelle werden die drei Elemente beschrieben, aus denen ein Windows Media-Download Paket besteht.</span><span class="sxs-lookup"><span data-stu-id="a5207-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="a5207-123">Package-Element</span><span class="sxs-lookup"><span data-stu-id="a5207-123">Package element</span></span>    | <span data-ttu-id="a5207-124">Funktion</span><span class="sxs-lookup"><span data-stu-id="a5207-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="a5207-125">Dateinamen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a5207-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="a5207-126">Rahmen</span><span class="sxs-lookup"><span data-stu-id="a5207-126">Border</span></span>             | <span data-ttu-id="a5207-127">Eine benutzerdefinierte, angepasste Benutzeroberfläche, die vom Besitzer des Inhalts zum Anzeigen, verknüpfen und Abspielen aller Medien, die im Windows Media-Download Paket verpackt sind, erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a5207-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="a5207-128">Die Verfahren zum Erstellen von Rahmen ähneln denen, die zum Erstellen von Skins verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5207-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="a5207-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="a5207-129">.wmz</span></span>                                     |
| <span data-ttu-id="a5207-130">Metafile-Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="a5207-130">Metafile Playlist</span></span>  | <span data-ttu-id="a5207-131">Eine Windows Media-Metadatendatei, die **Eintrags** Elemente, Wiedergabelisten Informationen und eine **Skin** -Element Identität für Inhalts Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="a5207-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="a5207-132">.asx</span><span class="sxs-lookup"><span data-stu-id="a5207-132">.asx</span></span>                                     |
| <span data-ttu-id="a5207-133">Multimedia-Inhalte</span><span class="sxs-lookup"><span data-stu-id="a5207-133">Multimedia Content</span></span> | <span data-ttu-id="a5207-134">Eine Datei, die ein beliebiges Audio-oder Videoformat enthält, das von Windows Media Player unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a5207-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="a5207-135">. WMA,. WMV,. ASF,. wav,. AVI,. mpg,. MP3</span><span class="sxs-lookup"><span data-stu-id="a5207-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a5207-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5207-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5207-137">**Windows Media-Download Pakete (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="a5207-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




