---
title: Objektmodell Referenz für die Skripterstellung
description: Objektmodell Referenz für die Skripterstellung
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player Mobile, Objektmodell
- Windows Media Player-Objektmodell, Referenz
- Objektmodell, Referenz
- ActiveX-Steuerelement, Referenz
- Windows Media Player ActiveX-Steuerelement, Referenz
- Windows Media Player Mobile ActiveX-Steuerelement, Referenz
- Referenz für Objektmodell, Skripterstellung
- Windows Media Player, Skript Referenz
- Windows Media Player Mobile, Skript Referenz
- Windows Media Player-Objektmodell, Skript Referenz
- Objektmodell, Skript Referenz
- Windows Media Player ActiveX-Steuerelement, Skript Referenz
- Windows Media Player Mobile ActiveX-Steuerelement, Skript Referenz
- ActiveX-Steuerelement, Skript Referenz
- Skript Objektmodell-Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342292"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="b2607-119">Objektmodell Referenz für die Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="b2607-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="b2607-120">Die Objektmodell Referenz für die Skripterstellung enthält ausführliche Informationen zum Windows Media Player ActiveX-Steuerelement Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="b2607-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="b2607-121">Die Informationen in diesem Abschnitt werden in einem Format dargestellt, das für die Verwendung mit Skriptsprachen wie Microsoft JScript konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="b2607-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="b2607-122">Alle Methoden, Eigenschaften und Ereignisse werden in Windows Media Player 10 Mobile oder höher vollständig unterstützt, sofern nicht ausdrücklich anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2607-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="b2607-123">Die Objektmodell Referenz für die Skripterstellung enthält Dokumentation für die folgenden Objekte und die zugehörigen Methoden, Eigenschaften und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b2607-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="b2607-124">Object</span><span class="sxs-lookup"><span data-stu-id="b2607-124">Object</span></span>                                              | <span data-ttu-id="b2607-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2607-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2607-126">Rom</span><span class="sxs-lookup"><span data-stu-id="b2607-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="b2607-127">Methoden und Eigenschaften für den Zugriff auf eine CD oder DVD auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="b2607-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="b2607-128">Cdromcollection</span><span class="sxs-lookup"><span data-stu-id="b2607-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="b2607-129">Methoden und Eigenschaften für den Zugriff auf eine Sammlung von CD-oder DVD-Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="b2607-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="b2607-130">Closedcaption</span><span class="sxs-lookup"><span data-stu-id="b2607-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="b2607-131">Eigenschaften zum Einschließen von Beschriftungen mit einem Medien Element.</span><span class="sxs-lookup"><span data-stu-id="b2607-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="b2607-132">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b2607-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="b2607-133">Methoden und Eigenschaften, die die Transport Steuerelemente von Windows Media Player darstellen, wie z. b. Wiedergabe, anhalten und anhalten.</span><span class="sxs-lookup"><span data-stu-id="b2607-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="b2607-134">DVD</span><span class="sxs-lookup"><span data-stu-id="b2607-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="b2607-135">Eine Eigenschaft, Methoden und Ereignisse für die Arbeit mit DVDs.</span><span class="sxs-lookup"><span data-stu-id="b2607-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="b2607-136">Fehler</span><span class="sxs-lookup"><span data-stu-id="b2607-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="b2607-137">Methoden und Eigenschaften, die den Zugriff auf eine Auflistung von **ErrorItem** -Objekten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b2607-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="b2607-138">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="b2607-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="b2607-139">Eigenschaften, die Informationen zu Fehlern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b2607-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="b2607-140">Medien</span><span class="sxs-lookup"><span data-stu-id="b2607-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="b2607-141">Methoden und Eigenschaften im Zusammenhang mit Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="b2607-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="b2607-142">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="b2607-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="b2607-143">Methoden, die Zugriff auf eine Auflistung von **Medien** Objekten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b2607-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="b2607-144">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="b2607-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="b2607-145">Eigenschaften zum Abrufen von Informationen zu den bildwerten des **WM/Bild-** metadatenattributs.</span><span class="sxs-lookup"><span data-stu-id="b2607-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="b2607-146">MetadataText</span><span class="sxs-lookup"><span data-stu-id="b2607-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="b2607-147">Eigenschaften zum Abrufen von Metadaten für komplexe textmetadatenattribute.</span><span class="sxs-lookup"><span data-stu-id="b2607-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="b2607-148">Network</span><span class="sxs-lookup"><span data-stu-id="b2607-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="b2607-149">Eigenschaften im Zusammenhang mit der Netzwerkverbindung von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b2607-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="b2607-150">Player</span><span class="sxs-lookup"><span data-stu-id="b2607-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="b2607-151">Methoden, Eigenschaften und Ereignisse, die von Windows Media Player programmiert werden können, um darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="b2607-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="b2607-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="b2607-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="b2607-153">Methoden und Eigenschaften für den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus des Players.</span><span class="sxs-lookup"><span data-stu-id="b2607-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="b2607-154">Kann nur mit C++-Programmen verwendet werden, die das-Steuerelement im Remote Modus einbetten.</span><span class="sxs-lookup"><span data-stu-id="b2607-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="b2607-155">Abspielen</span><span class="sxs-lookup"><span data-stu-id="b2607-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="b2607-156">Methoden und Eigenschaften zum Bearbeiten von Listen von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="b2607-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="b2607-157">Playlistarray</span><span class="sxs-lookup"><span data-stu-id="b2607-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="b2607-158">Eine-Methode und eine-Eigenschaft für den Zugriff auf eine Auflistung von **Wiedergabe** Listen Objekten nach Indexnummer.</span><span class="sxs-lookup"><span data-stu-id="b2607-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="b2607-159">Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="b2607-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="b2607-160">Methoden zum Organisieren einer Auflistung von **Wiedergabe** Listen Objekten.</span><span class="sxs-lookup"><span data-stu-id="b2607-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="b2607-161">Abfrage</span><span class="sxs-lookup"><span data-stu-id="b2607-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="b2607-162">Methoden zum Ändern einer Verbund Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b2607-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="b2607-163">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b2607-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="b2607-164">Eigenschaften, die die Angabe oder den Abruf von Windows Media Player-Einstellungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b2607-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="b2607-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="b2607-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="b2607-166">Eine-Methode und eine-Eigenschaft zum Bearbeiten von Zeichen folgen Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="b2607-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b2607-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2607-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2607-168">**Referenz zum Windows Media Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="b2607-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 




