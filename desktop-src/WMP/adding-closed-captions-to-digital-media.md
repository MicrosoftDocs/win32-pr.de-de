---
title: Hinzufügen von Untertiteln zu digitalen Medien
description: Hinzufügen von Untertiteln zu digitalen Medien
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Informationen zu
- Sami (synchronisierter, zugänglicher Medienaustausch), Informationen zu
- Windows Media Player, Hinzufügen von Untertiteln
- Windows Media Player-Objektmodell, Hinzufügen von Untertiteln
- Objektmodell, Hinzufügen von Untertiteln
- Windows Media Player Mobile, Hinzufügen von Untertiteln
- Windows Media Player ActiveX-Steuerelement, Hinzufügen von Untertiteln
- Windows Media Player Mobile ActiveX-Steuerelement, Hinzufügen von Untertiteln
- ActiveX-Steuerelement, Hinzufügen von Untertiteln
- Synchronisierter, barrierefreier Medienaustausch (Sami), Hinzufügen von Untertiteln
- Sami (synchronisierter, zugänglicher Medienaustausch), Hinzufügen von Untertiteln
- Hinzufügen von Untertiteln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036634"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="123f4-122">Hinzufügen von Untertiteln zu digitalen Medien</span><span class="sxs-lookup"><span data-stu-id="123f4-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="123f4-123">Der synchronisierte, barrierefreie Medienaustausch (Sami) ist ein Dateiformat, das für die Bereitstellung von synchronisiertem Text wie Beschriftungen, Untertiteln oder Audiobeschreibungen mit digitalen Medieninhalten konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="123f4-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="123f4-124">Mit dem Windows Media Player-Objektmodell in einen Webbrowser integriert, wird die Barrierefreiheit von Sami herauf gestuft.</span><span class="sxs-lookup"><span data-stu-id="123f4-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="123f4-125">Mit Sami können Sie Rich-Media-Inhalte erstellen, die eine größere, vielfältigere Zielgruppe erreichen.</span><span class="sxs-lookup"><span data-stu-id="123f4-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="123f4-126">Neben den Standard Schriftarten kann Sami auch andere Text Stile unterstützen, wie z. b. unterschiedliche Farben, Größen oder Sprachen, um eine Vielzahl von Benutzern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="123f4-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="123f4-127">Sami kann besonders nützlich für Personen mit Sehfähigkeit oder Hörgeschädigte sein, die gehörlos oder hörgeschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="123f4-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="123f4-128">Das SAMI-Format kann auch für Schulungszwecke hilfreich sein, z. b. für Schüler und Studenten eine zweite Sprache.</span><span class="sxs-lookup"><span data-stu-id="123f4-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="123f4-129">Dieses Thema konzentriert sich auf die Einbindung von Sami in das Windows Media Player ActiveX-Steuerelement Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="123f4-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="123f4-130">Sami-Dateien sind unabhängig von digitalen Mediendateien vorhanden und beruhen nicht darauf, dass ein bestimmtes Video-oder Audioformat funktioniert.</span><span class="sxs-lookup"><span data-stu-id="123f4-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="123f4-131">Da die Dateien getrennt sind, wird das Windows Media Player-Steuerelement die einzelnen Dateien auf dem Client Computer suchen, analysieren, synchronisieren und Rendering.</span><span class="sxs-lookup"><span data-stu-id="123f4-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="123f4-132">Dies bietet zusätzliche Flexibilität und Funktionalität, da Sie die Bearbeitung von einzelnen samappendateien, die Einbindung der Sami-Datei in verschiedene digitale Medienformate und die Speicherung von samappendateien an verschiedenen Serverstandorten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="123f4-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="123f4-133">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="123f4-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="123f4-134">`Section`</span><span class="sxs-lookup"><span data-stu-id="123f4-134">Section</span></span>                                                                                                                            | <span data-ttu-id="123f4-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="123f4-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="123f4-136">Informationen zu Sami-Dateien</span><span class="sxs-lookup"><span data-stu-id="123f4-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="123f4-137">Beschreibt die grundlegende Struktur von sasafiles.</span><span class="sxs-lookup"><span data-stu-id="123f4-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="123f4-138">Beispiel für Sami-Datei</span><span class="sxs-lookup"><span data-stu-id="123f4-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="123f4-139">Beschreibt die Struktur einer Beispiel-Sami-Datei.</span><span class="sxs-lookup"><span data-stu-id="123f4-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="123f4-140">Verwenden von Sami mit dem Windows Media Player-Steuerelement in einem Browser</span><span class="sxs-lookup"><span data-stu-id="123f4-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="123f4-141">Beschreibt die Verwendung von Sami in einer Webseite mit dem Windows Media Player-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="123f4-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="123f4-142">Informationen zu Sami-URLs</span><span class="sxs-lookup"><span data-stu-id="123f4-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="123f4-143">Hier wird beschrieben, wie Sie mit einer einzelnen URL in den samappendateien mit Sami-Dateien verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="123f4-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="123f4-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="123f4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="123f4-145">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="123f4-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




