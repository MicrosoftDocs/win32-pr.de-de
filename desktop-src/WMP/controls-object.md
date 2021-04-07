---
title: Controls-Objekt
description: Das Steuerelement-Objekt bietet eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu manipulieren.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Steuert Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "103718948"
---
# <a name="controls-object"></a><span data-ttu-id="02332-104">Controls-Objekt</span><span class="sxs-lookup"><span data-stu-id="02332-104">Controls Object</span></span>

<span data-ttu-id="02332-105">Das Steuerelement **-Objekt bietet** eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu manipulieren.</span><span class="sxs-lookup"><span data-stu-id="02332-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="02332-106">Das Steuerelement **-Objekt unterstützt die folgenden** Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02332-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="02332-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02332-107">Property</span></span>                                                            | <span data-ttu-id="02332-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02332-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02332-109">audiolanguagecount</span><span class="sxs-lookup"><span data-stu-id="02332-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="02332-110">Ruft die Anzahl der unterstützten Audiosprachen ab.</span><span class="sxs-lookup"><span data-stu-id="02332-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="02332-111">currentaudiolanguage</span><span class="sxs-lookup"><span data-stu-id="02332-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="02332-112">Gibt den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="02332-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="02332-113">currentaudiolanguageindex</span><span class="sxs-lookup"><span data-stu-id="02332-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="02332-114">Gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="02332-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="02332-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="02332-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="02332-116">Gibt das aktuelle Medien Element an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="02332-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="02332-117">currentmarker</span><span class="sxs-lookup"><span data-stu-id="02332-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="02332-118">Gibt die aktuelle Markernummer an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="02332-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="02332-119">CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="02332-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="02332-120">Gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="02332-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="02332-121">currentpositionstring</span><span class="sxs-lookup"><span data-stu-id="02332-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="02332-122">Ruft die aktuelle Position im Medien Element als **Zeichenfolge** ab.</span><span class="sxs-lookup"><span data-stu-id="02332-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="02332-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="02332-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="02332-124">Gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="02332-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="02332-125">Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="02332-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="02332-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="02332-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="02332-127">Ruft ab, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="02332-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="02332-128">Das Steuerelement **-Objekt unterstützt die folgenden** Methoden.</span><span class="sxs-lookup"><span data-stu-id="02332-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="02332-129">Methode</span><span class="sxs-lookup"><span data-stu-id="02332-129">Method</span></span>                                                                  | <span data-ttu-id="02332-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02332-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02332-131">FastForward</span><span class="sxs-lookup"><span data-stu-id="02332-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="02332-132">Startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.</span><span class="sxs-lookup"><span data-stu-id="02332-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="02332-133">fastreverse</span><span class="sxs-lookup"><span data-stu-id="02332-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="02332-134">Startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="02332-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="02332-135">getaudiolanguagedescription</span><span class="sxs-lookup"><span data-stu-id="02332-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="02332-136">Ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="02332-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="02332-137">getaudiolanguageid</span><span class="sxs-lookup"><span data-stu-id="02332-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="02332-138">Ruft die LCID für einen angegebenen audiosprachindex ab.</span><span class="sxs-lookup"><span data-stu-id="02332-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="02332-139">getlanguagename</span><span class="sxs-lookup"><span data-stu-id="02332-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="02332-140">Ruft den Namen der Audiosprache mit der angegebenen LCID ab.</span><span class="sxs-lookup"><span data-stu-id="02332-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="02332-141">Weiter</span><span class="sxs-lookup"><span data-stu-id="02332-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="02332-142">Legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.</span><span class="sxs-lookup"><span data-stu-id="02332-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="02332-143">pause</span><span class="sxs-lookup"><span data-stu-id="02332-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="02332-144">Hält die Wiedergabe des Medien Elements an.</span><span class="sxs-lookup"><span data-stu-id="02332-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="02332-145">Theater</span><span class="sxs-lookup"><span data-stu-id="02332-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="02332-146">Bewirkt, dass das Medien Element wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02332-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="02332-147">PlayItem</span><span class="sxs-lookup"><span data-stu-id="02332-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="02332-148">Bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder setzt die Wiedergabe eines angehaltenen Elements fort.</span><span class="sxs-lookup"><span data-stu-id="02332-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="02332-149">previous</span><span class="sxs-lookup"><span data-stu-id="02332-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="02332-150">Legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.</span><span class="sxs-lookup"><span data-stu-id="02332-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="02332-151">Schritt</span><span class="sxs-lookup"><span data-stu-id="02332-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="02332-152">Bewirkt, dass das aktuelle Video Medien Element die Wiedergabe im nächsten Frame fixiert.</span><span class="sxs-lookup"><span data-stu-id="02332-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="02332-153">stop</span><span class="sxs-lookup"><span data-stu-id="02332-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="02332-154">Beendet die Wiedergabe des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="02332-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="02332-155">Der Zugriff auf das Steuerelement Objekt erfolgt **über die folgende** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="02332-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="02332-156">Object</span><span class="sxs-lookup"><span data-stu-id="02332-156">Object</span></span>                      | <span data-ttu-id="02332-157">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02332-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="02332-158">Player</span><span class="sxs-lookup"><span data-stu-id="02332-158">Player</span></span>](player-object.md) | [<span data-ttu-id="02332-159">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="02332-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="02332-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02332-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02332-161">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="02332-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




