---
title: Informationen zum Player-Objektmodell
description: Informationen zum Player-Objektmodell
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Informationen zu
- Objektmodell, Informationen
- Windows Media Player ActiveX-Steuerelement, Objektmodell
- ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Objektmodell
- Windows Media Player Mobile, Objektmodell
- Software Development Kit (SDK), Windows Media Player ActiveX-Steuerelement-Objektmodell
- SDK (Software Development Kit), Windows Media Player ActiveX-Steuerelement-Objektmodell
- Dokumentation, Windows Media Player ActiveX-Steuerelement-Objektmodell
- Player-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340841"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="1b2d4-114">Informationen zum Player-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="1b2d4-114">About the Player Object Model</span></span>

<span data-ttu-id="1b2d4-115">Das Microsoft Windows Media Player-Steuerelement ist ein ActiveX-Standard Steuerelement, das die Microsoft Component Object Model (com)-Technologie verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="1b2d4-116">Die Windows Media Player-Funktionalität wird in eine Reihe von Programmierschnittstellen unterteilt, die den Standard-com-Richtlinien folgen.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="1b2d4-117">Sie können diese Schnittstellen auf einer HTML-Standard Webseite programmieren, indem Sie das Steuerelement Objektmodell von Player mit Microsoft JScript oder Microsoft Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="1b2d4-118">Sie können Sie auch mithilfe von Microsoft JScript in Skins programmieren.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="1b2d4-119">Wenn Sie ein benutzerdefiniertes Programm erstellen möchten, das das Steuerelement einbettet, können Sie eine von mehreren Sprachen verwenden, einschließlich Visual Basic, C++ und c#.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="1b2d4-120">Das Windows Media Player ActiveX-Steuerelement wird mit Windows Media Player installiert.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="1b2d4-121">Das Player-Steuerelement wird nicht mit dem Windows Media Player SDK installiert und kann nicht separat neu verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="1b2d4-122">Welche Funktionen für Ihren Code verfügbar sind, hängt davon ab, welche Version von Windows Media Player der Benutzer installiert hat.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="1b2d4-123">Die [Objektmodell Referenz für die Skript](object-model-reference-for-scripting.md) -und [Objektmodell Referenz für C++](object-model-reference-for-c.md) enthält Informationen zu den Versions Anforderungen für die einzelnen Eigenschaften, Methoden und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="1b2d4-124">In den folgenden Abschnitten finden Sie eine Übersicht über das Windows Media Player-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="1b2d4-125">`Section`</span><span class="sxs-lookup"><span data-stu-id="1b2d4-125">Section</span></span>                                                                                        | <span data-ttu-id="1b2d4-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b2d4-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b2d4-127">Player-Objektmodell für Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="1b2d4-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="1b2d4-128">In diesem Abschnitt werden die Objekte beschrieben, die im Objektmodell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="1b2d4-129">Informationen zu Objektmodellversionen</span><span class="sxs-lookup"><span data-stu-id="1b2d4-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="1b2d4-130">In diesem Abschnitt wird erläutert, welche Objektmodell Elemente in jeder Version seit der Einführung von Windows Media Player 7,0 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="1b2d4-131">Eigenschaften, Methoden und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1b2d4-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="1b2d4-132">In diesem Abschnitt werden Eigenschaften, Methoden und Ereignisse erläutert.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="1b2d4-133">Unterstützte Protokolle und Dateitypen</span><span class="sxs-lookup"><span data-stu-id="1b2d4-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="1b2d4-134">In diesem Abschnitt werden die Protokolle und Dateitypen aufgelistet, die von Windows Media Player und dem Windows Media Player Control-Objektmodell unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="1b2d4-135">Informationen zur Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b2d4-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="1b2d4-136">In diesem Abschnitt wird die Windows Media Player-Bibliothek beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="1b2d4-137">Verwenden von HTML mit Windows-Media Player</span><span class="sxs-lookup"><span data-stu-id="1b2d4-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="1b2d4-138">In diesem Abschnitt werden die verschiedenen Möglichkeiten beschrieben, wie Windows Media Player und HTML zusammenarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="1b2d4-139">Einbetten des Windows Media Player-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="1b2d4-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="1b2d4-140">In diesem Abschnitt werden die verschiedenen Möglichkeiten zum Einbetten des Windows Media Player-Steuer Elements in Microsoft Office Dokumente und benutzerdefinierte Programme beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="1b2d4-141">Informationen zur Geräte Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="1b2d4-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="1b2d4-142">In diesem Abschnitt werden die Funktionen beschrieben, die vom Windows Media Player 10-Steuerelement für die Übertragung digitaler Medieninhalte auf tragbare Geräte bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="1b2d4-143">Informationen zum Brennen von CDs</span><span class="sxs-lookup"><span data-stu-id="1b2d4-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="1b2d4-144">In diesem Abschnitt werden die Funktionen beschrieben, die das Windows Media Player-Steuerelement zum Erstellen von CDs bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="1b2d4-145">Informationen zum CD-Ripping</span><span class="sxs-lookup"><span data-stu-id="1b2d4-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="1b2d4-146">In diesem Abschnitt werden die Funktionen beschrieben, die vom Windows Media Player-Steuerelement zum Kopieren von Titeln von AudioCDs auf den Computer des Benutzers bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="1b2d4-147">Informationen zur Ordner Überwachung</span><span class="sxs-lookup"><span data-stu-id="1b2d4-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="1b2d4-148">In diesem Abschnitt werden die Funktionen beschrieben, die vom Windows Media Player-Steuerelement zum Steuern der Ordner Überwachungsprozesse des Players bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2d4-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="1b2d4-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b2d4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b2d4-150">**Windows Media Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="1b2d4-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




