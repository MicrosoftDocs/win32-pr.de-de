---
title: Player-Element
description: Player-Element
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player Skins, Player-Element
- Skins, Player-Element
- Player-Element
- Verweis für Skins, Player-Element
- Elemente, Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100758"
---
# <a name="player-element"></a><span data-ttu-id="f6134-108">Player-Element</span><span class="sxs-lookup"><span data-stu-id="f6134-108">PLAYER Element</span></span>

<span data-ttu-id="f6134-109">Das **Player** -Element ermöglicht Ihnen das Definieren von Ereignis Handlern und das Angeben der **URL** -Eigenschaft des **Player** -Objekts zur Entwurfszeit in einer Skin-Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="f6134-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="f6134-110">Innerhalb von Skriptcode erfolgt der Zugriff auf das **Player** -Objekt über das globale Attribut des **Players** anstelle eines Namens, der durch ein **ID** -Attribut angegeben wird. Dies wird vom **Player** -Element nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6134-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="f6134-111">Das **Player** -Element unterstützt das folgende Attribut.</span><span class="sxs-lookup"><span data-stu-id="f6134-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="f6134-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="f6134-112">Attribute</span></span>             | <span data-ttu-id="f6134-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6134-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="f6134-114">URL</span><span class="sxs-lookup"><span data-stu-id="f6134-114">URL</span></span>](player-url.md) | <span data-ttu-id="f6134-115">Gibt den Namen der Datei an, die wiedergegeben werden soll, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f6134-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="f6134-116">Das **Player** -Element kann Ereignishandler für die folgenden Ereignisse implementieren, die aus dem **Player** -Objekt ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f6134-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="f6134-117">Ereignis</span><span class="sxs-lookup"><span data-stu-id="f6134-117">Event</span></span>                                                                                            | <span data-ttu-id="f6134-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6134-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="f6134-119">Audiolanguagechange</span><span class="sxs-lookup"><span data-stu-id="f6134-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="f6134-120">Tritt auf, wenn sich die aktuelle Audiosprache ändert.</span><span class="sxs-lookup"><span data-stu-id="f6134-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="f6134-121">Pufferung</span><span class="sxs-lookup"><span data-stu-id="f6134-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="f6134-122">Tritt auf, wenn Windows Media Player Pufferung startet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="f6134-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="f6134-123">Cdrommediachange</span><span class="sxs-lookup"><span data-stu-id="f6134-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="f6134-124">Tritt auf, wenn das CD-Medium geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="f6134-125">Ereignis Wechsel</span><span class="sxs-lookup"><span data-stu-id="f6134-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="f6134-126">Tritt ein, wenn das aktuelle Element geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="f6134-127">Currentmediaitemavailable</span><span class="sxs-lookup"><span data-stu-id="f6134-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="f6134-128">Tritt ein, wenn das aktuelle Medien Element verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="f6134-129">Currentplaylistchange</span><span class="sxs-lookup"><span data-stu-id="f6134-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="f6134-130">Tritt ein, wenn die aktuelle Wiedergabeliste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="f6134-131">Currentplaylistitemavailable</span><span class="sxs-lookup"><span data-stu-id="f6134-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="f6134-132">Tritt ein, wenn das aktuelle Wiedergabelisten Element verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="f6134-133">Domainchange</span><span class="sxs-lookup"><span data-stu-id="f6134-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="f6134-134">Tritt auf, wenn die DVD-Domäne geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="f6134-135">Fehler</span><span class="sxs-lookup"><span data-stu-id="f6134-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="f6134-136">Tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="f6134-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="f6134-137">Markerhit</span><span class="sxs-lookup"><span data-stu-id="f6134-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="f6134-138">Tritt auf, wenn ein Windows-Media Player einen Marker im Clip trifft.</span><span class="sxs-lookup"><span data-stu-id="f6134-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="f6134-139">Mediachange</span><span class="sxs-lookup"><span data-stu-id="f6134-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="f6134-140">Tritt auf, wenn ein Medien Element geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="f6134-141">Mediacollectionattributestringadded</span><span class="sxs-lookup"><span data-stu-id="f6134-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="f6134-142">Tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="f6134-143">Mediacollectionattributestringchanged</span><span class="sxs-lookup"><span data-stu-id="f6134-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="f6134-144">Tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="f6134-145">Mediacollectionattributestraningrebewegt</span><span class="sxs-lookup"><span data-stu-id="f6134-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="f6134-146">Tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="f6134-147">Mediacollectionchange</span><span class="sxs-lookup"><span data-stu-id="f6134-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="f6134-148">Tritt auf, wenn das **mediacollection** -Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="f6134-149">MediaError</span><span class="sxs-lookup"><span data-stu-id="f6134-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="f6134-150">Tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="f6134-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="f6134-151">Modeänderung</span><span class="sxs-lookup"><span data-stu-id="f6134-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="f6134-152">Tritt beim Wechseln zwischen dem shuffle-und dem Normalmodus auf.</span><span class="sxs-lookup"><span data-stu-id="f6134-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="f6134-153">Openplaylistswitch</span><span class="sxs-lookup"><span data-stu-id="f6134-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="f6134-154">Tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.</span><span class="sxs-lookup"><span data-stu-id="f6134-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="f6134-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="f6134-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="f6134-156">Tritt auf, wenn der *Player*. **openstate** -Änderungen.</span><span class="sxs-lookup"><span data-stu-id="f6134-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="f6134-157">Playlistchange</span><span class="sxs-lookup"><span data-stu-id="f6134-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="f6134-158">Tritt auf, wenn eine Wiedergabeliste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="f6134-159">Playlistcollectionchange</span><span class="sxs-lookup"><span data-stu-id="f6134-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="f6134-160">Tritt auf, wenn sich etwas in der Wiedergabelisten Auflistung ändert.</span><span class="sxs-lookup"><span data-stu-id="f6134-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="f6134-161">Playlistcollectionplaylistadded</span><span class="sxs-lookup"><span data-stu-id="f6134-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="f6134-162">Tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="f6134-163">Playlistcollectionplaylistreverschohe</span><span class="sxs-lookup"><span data-stu-id="f6134-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="f6134-164">Tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="f6134-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="f6134-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="f6134-166">Tritt auf, wenn der *Player*. **playstate** ändert sich.</span><span class="sxs-lookup"><span data-stu-id="f6134-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="f6134-167">Positionsänderung</span><span class="sxs-lookup"><span data-stu-id="f6134-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="f6134-168">Tritt auf, wenn der *Player*. -Steuer *Elemente*. **CurrentPosition** ändert sich.</span><span class="sxs-lookup"><span data-stu-id="f6134-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="f6134-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="f6134-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="f6134-170">Tritt auf, wenn Windows Media Player einen in eine Datei eingebetteten Skript Befehl trifft.</span><span class="sxs-lookup"><span data-stu-id="f6134-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="f6134-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="f6134-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="f6134-172">Tritt ein, wenn der Wert der **Status** Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6134-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="f6134-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6134-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6134-174">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f6134-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f6134-175">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="f6134-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




