---
title: Verwenden von HTML mit Windows-Media Player
description: Verwenden von HTML mit Windows-Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Windows Media Player-Objektmodell, HTML
- Objektmodell, HTML
- Windows Media Player ActiveX-Steuerelement, HTML für Objektmodell
- ActiveX-Steuerelement, HTML für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, HTML für Objektmodell
- Windows Media Player Mobile, HTML für Objektmodell
- HTML mit Windows-Media Player
- Einbettung von Webseiten, HTML
- Einbettungen, Webseiten
- Skript Befehle
- URL-kippen
- Rich-Media-Streaming
- Browserunterstützung
- Anzeigen von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856263"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="9a990-118">Verwenden von HTML mit Windows-Media Player</span><span class="sxs-lookup"><span data-stu-id="9a990-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="9a990-119">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9a990-119">Overview</span></span>

<span data-ttu-id="9a990-120">Die Verwendung von HTML mit Windows Media Player ist eine hervorragende Möglichkeit, um Audioinhalte und Videos mit Text und Grafiken zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="9a990-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="9a990-121">Sie können das Windows Media Player-Steuerelement in eine Webseite einbetten, wenn Sie Ihre statischen Inhalte ergänzen oder Webanwendungen mit digitalen Medien erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9a990-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="9a990-122">Wenn Sie Ihre digitalen Medien mit HTML ergänzen möchten, können Sie Webseiten im vollständigen Modus des Players anzeigen, indem Sie in den Windows Media Metadatei-Wiedergabelisten auf Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="9a990-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="9a990-123">Wenn Sie benutzerdefinierte Programme schreiben, die das Windows Media Player-Steuerelement im Remote Modus einbetten, können Sie auch die Webseiten steuern, die in den verschiedenen Bereichen des vollständigen Modus des Players angezeigt werden, wenn die Benutzer das Steuerelement Abdocken.</span><span class="sxs-lookup"><span data-stu-id="9a990-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="9a990-124">Auf diese Weise können Sie die Kontinuität zwischen angedockten und nicht angedockten Zuständen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9a990-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="9a990-125">Webeinbettung</span><span class="sxs-lookup"><span data-stu-id="9a990-125">Web Embedding</span></span>

<span data-ttu-id="9a990-126">Sie können das Windows Media Player-Steuerelement als Teil einer Webseite verwenden, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a990-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="9a990-127">Informationen finden Sie [unter Einbetten des Windows Media Player-Steuer Elements in eine Webseite](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="9a990-128">Skript Befehle und URL-Flipping</span><span class="sxs-lookup"><span data-stu-id="9a990-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="9a990-129">Skript Befehle sind Text/Wert-Paare, die Sie in Ihre digitalen Mediendateien oder Streams einbetten können.</span><span class="sxs-lookup"><span data-stu-id="9a990-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="9a990-130">Sie können benutzerdefinierte Skript Befehle ausschließlich zum Lösen von Skriptcode verwenden, während Windows Media Player anderen Skript Befehlen automatisch verarbeiten lässt.</span><span class="sxs-lookup"><span data-stu-id="9a990-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="9a990-131">Wenn Sie über mehrere Webseiten verfügen, die eine digitale Medienpräsentation begleiten, können URL-Skript Befehle die Seite automatisch in einem Frame ändern, während das Windows Media Player-Steuerelement weiterhin digitale Medien in einem anderen Frame wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="9a990-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="9a990-132">Dies wird als URL-Flipping bezeichnet und ist eine hervorragende Möglichkeit zum Erstellen einer Multimedia-Folien Anzeige.</span><span class="sxs-lookup"><span data-stu-id="9a990-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="9a990-133">Mit anderen automatisch behandelten Skript Befehlen können Sie die Wiedergabe in eine andere Mediendatei oder einen anderen Stream umschalten, Beschriftungs Text anzeigen oder Ereignisse wie AD-Einfügungen Auslöschungen, die in einer Windows Media Metadatei-Wiedergabeliste definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9a990-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="9a990-134">Weitere Informationen zum Überspringen von URLs finden Sie unter [Erstellen von Web-Based Präsentationen](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="9a990-135">Rich-Media-Streaming</span><span class="sxs-lookup"><span data-stu-id="9a990-135">Rich Media Streaming</span></span>

<span data-ttu-id="9a990-136">Das URL-kippen funktioniert am besten mit einfachen Seiten, die schnell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9a990-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="9a990-137">Bei komplexeren Seiten werden mehrere Komponenten einzeln übertragen, was das Synchronisieren der Seiten Anzeige mit digitalen Medien erschwert.</span><span class="sxs-lookup"><span data-stu-id="9a990-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="9a990-138">Zum zulassen komplexer Rich-Media-Präsentationen können Webseiten einem Mediendaten Strom hinzugefügt und auf die gleiche Weise wie Audioinformationen und Videos an den Player übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9a990-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="9a990-139">Auf diese Weise können Sie die Komponenten Ihrer Präsentation viel einfacher synchronisieren, insbesondere über Verbindungen mit geringer Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="9a990-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="9a990-140">Weitere Informationen zum Streaming von Rich-Media-Medien finden Sie unter [Erstellen von Web-Based Präsentationen](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="9a990-141">Browserunterstützung</span><span class="sxs-lookup"><span data-stu-id="9a990-141">Browser Support</span></span>

<span data-ttu-id="9a990-142">Sie können das Windows Media Player-Steuerelement in Microsoft Internet Explorer, Firefox und Netscape Navigator einbetten, obwohl der Prozess für jeden Prozess etwas unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="9a990-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="9a990-143">Sie können auch Webseiten erstellen, die für alle drei Browser entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="9a990-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="9a990-144">Mit Internet Explorer und Firefox Betten Sie das Steuerelement mithilfe des HTML-Objekt Elements ein.</span><span class="sxs-lookup"><span data-stu-id="9a990-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="9a990-145">Der Navigator erfordert jedoch einen anderen Ansatz, da ActiveX-Steuerelemente nicht direkt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9a990-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="9a990-146">Mit Navigator verwenden Sie das Applet-Element, um ein spezielles Java-Applet in die Seite einzubetten.</span><span class="sxs-lookup"><span data-stu-id="9a990-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="9a990-147">Dieses Applet verarbeitet die Kommunikation mit dem Player-ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9a990-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="9a990-148">Weitere Informationen zur Unterstützung von Firefox finden [Sie unter Verwenden des Windows Media Player-Steuer Elements mit Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="9a990-149">Weitere Informationen zur Unterstützung von Netscape Navigator finden [Sie unter Verwenden von Windows Media Player mit Netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="9a990-150">Anzeigen von Webseiten im vollständigen Modus des Players</span><span class="sxs-lookup"><span data-stu-id="9a990-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="9a990-151">Sie können die Funktionalität von Windows Media Player erweitern oder eine benutzerdefinierte Ansicht der Informationen bereitstellen, die Ihre digitalen Medien enthalten, indem Sie Webseiten im vollständigen Modus des Players anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a990-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="9a990-152">Dies ist die HtmlView-Funktion von Windows Media-Metafiles.</span><span class="sxs-lookup"><span data-stu-id="9a990-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="9a990-153">Metadatendateien ermöglichen Ihnen eine hervorragende Kontrolle über den Wiedergabelisten Inhalt, sodass Sie nahtlos zwischen Clips wechseln, Ankündigungen einfügen und weiterhin Bilder in Windows Media Player anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="9a990-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="9a990-154">Wenn Sie Webseiten im vollständigen Modus des Players anzeigen möchten, verwenden Sie das param-Element, um Ihren Wiedergabelisten Einträgen oder vollständigen Wiedergabelisten URL-Verweise hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9a990-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="9a990-155">Weitere Informationen zur Verwendung von Webseiten in Metadateien finden Sie unter [Anzeigen von Webseiten in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="9a990-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a990-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a990-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a990-157">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="9a990-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




