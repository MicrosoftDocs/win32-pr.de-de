---
title: Player-Objektmodell für Skriptsprachen
description: Player-Objektmodell für Skriptsprachen
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
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
- Windows Media Player, Skriptsprachen
- Windows Media Player-Objektmodell, Skriptsprachen
- Objektmodell, Skriptsprachen
- Windows Media Player ActiveX-Steuerelement, Skriptsprachen
- ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobile ActiveX-Steuerelement, Skriptsprachen
- Windows Media Player Mobile, Skriptsprachen
- Skriptsprachen
- Windows Media Player, Player-Objekt
- Windows Media Player-Objektmodell, Player-Objekt
- Objektmodell, Player-Objekt
- Windows Media Player ActiveX-Steuerelement, Player-Objekt
- ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Player-Objekt
- Windows Media Player Mobile, Player-Objekt
- Player-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570737"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="36d04-129">Player-Objektmodell für Skriptsprachen</span><span class="sxs-lookup"><span data-stu-id="36d04-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="36d04-130">ActiveX verwendet das Konzept von-Objekten, um Programmierfunktionen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="36d04-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="36d04-131">In Windows Media Player werden mehrere-Objekte verwendet, um die Funktionalität des Steuer Elements aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="36d04-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="36d04-132">Das Stamm Objekt ist das **Player** -Objekt, und die anderen Objekte werden über bestimmte Eigenschaften an das **Player** -Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="36d04-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="36d04-133">Das folgende Diagramm zeigt, wie das Objektmodell des ActiveX-Steuer Elements von Windows Media Player 11 für Skriptsprachen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="36d04-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![Diagramm des Windows Media Player 11-Objektmodells](images/playeromdiag.png)

<span data-ttu-id="36d04-135">In C++ und manchmal in .NET-Sprachen werden Objekte durch COM-Schnittstellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="36d04-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="36d04-136">Im Windows Media Player-Objektmodell Stimmen com-Schnittstellennamen mit dem Objektnamen überein, haben jedoch das Präfix "iwmp".</span><span class="sxs-lookup"><span data-stu-id="36d04-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="36d04-137">Das **Netzwerk** Objekt wird z. b. über die **iwmpnetwork** -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="36d04-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="36d04-138">In den folgenden Abschnitten werden konzeptionelle Übersichten für jedes Objekt bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="36d04-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="36d04-139">Informationen zu den CDROM-und cdromcollection-Objekten</span><span class="sxs-lookup"><span data-stu-id="36d04-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="36d04-140">Informationen zum closedcaption-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="36d04-141">Informationen zum Steuerelement Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="36d04-142">Informationen zum DVD-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="36d04-143">Informationen zu den Fehlern und ErrorItem-Objekten</span><span class="sxs-lookup"><span data-stu-id="36d04-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="36d04-144">Informationen zu mediacollection und Media Objects</span><span class="sxs-lookup"><span data-stu-id="36d04-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="36d04-145">Informationen zum MetadataPicture-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="36d04-146">Informationen zum MetadataText-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="36d04-147">Informationen zum Netzwerk Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="36d04-148">Informationen zum Player-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="36d04-149">Informationen zum playerapplication-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="36d04-150">Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten</span><span class="sxs-lookup"><span data-stu-id="36d04-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="36d04-151">Informationen zum Query-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="36d04-152">Informationen zum Einstellungs Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="36d04-153">Informationen zum StringCollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="36d04-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="36d04-154">Zusätzliche Funktionen sind über bestimmte COM-Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36d04-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="36d04-155">Ob Sie auf diese Schnittstellen zugreifen können, hängt möglicherweise von der Sprache, die Sie für die Programmierung verwenden, und anderen Faktoren ab, wie z. b. dem Modus, der zum Erstellen der Instanz des Windows-Media Player</span><span class="sxs-lookup"><span data-stu-id="36d04-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="36d04-156">Eine umfassende Liste der COM-Schnittstellen, die vom Windows Media Player-Steuerelement verfügbar gemacht werden, finden Sie in der [Objektmodell Referenz für C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="36d04-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36d04-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36d04-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36d04-158">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="36d04-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="36d04-159">**Verwenden des Windows Media Player-Steuer Elements in einer .NET Framework-Lösung**</span><span class="sxs-lookup"><span data-stu-id="36d04-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




