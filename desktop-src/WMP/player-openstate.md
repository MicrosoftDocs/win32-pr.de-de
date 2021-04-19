---
title: Player. openstate
description: Die openstate-Eigenschaft ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. openstate-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367531"
---
# <a name="playeropenstate"></a><span data-ttu-id="707b8-104">Player. openstate</span><span class="sxs-lookup"><span data-stu-id="707b8-104">Player.openState</span></span>

<span data-ttu-id="707b8-105">Die **openstate** -Eigenschaft ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.</span><span class="sxs-lookup"><span data-stu-id="707b8-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="707b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="707b8-106">Syntax</span></span>

<span data-ttu-id="707b8-107">*Player* . **openstate**</span><span class="sxs-lookup"><span data-stu-id="707b8-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="707b8-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="707b8-108">Possible Values</span></span>

<span data-ttu-id="707b8-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="707b8-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="707b8-110">Die Enumerationskonstante im C-Stil kann durch Voranstellen des Zustands Werts mit "wmpos" abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="707b8-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="707b8-111">Beispielsweise ist die Konstante für den playlistopening-Zustand **wmposplaylistopening**.</span><span class="sxs-lookup"><span data-stu-id="707b8-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="707b8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="707b8-112">Value</span></span> | <span data-ttu-id="707b8-113">State</span><span class="sxs-lookup"><span data-stu-id="707b8-113">State</span></span>                   | <span data-ttu-id="707b8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="707b8-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707b8-115">0</span><span class="sxs-lookup"><span data-stu-id="707b8-115">0</span></span>     | <span data-ttu-id="707b8-116">Nicht definiert</span><span class="sxs-lookup"><span data-stu-id="707b8-116">Undefined</span></span>               | <span data-ttu-id="707b8-117">Windows Media Player befindet sich in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="707b8-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="707b8-118">1</span><span class="sxs-lookup"><span data-stu-id="707b8-118">1</span></span>     | <span data-ttu-id="707b8-119">Playlistchanging</span><span class="sxs-lookup"><span data-stu-id="707b8-119">PlaylistChanging</span></span>        | <span data-ttu-id="707b8-120">Neue Wiedergabeliste wird geladen.</span><span class="sxs-lookup"><span data-stu-id="707b8-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="707b8-121">2</span><span class="sxs-lookup"><span data-stu-id="707b8-121">2</span></span>     | <span data-ttu-id="707b8-122">Playlistlokalisierung</span><span class="sxs-lookup"><span data-stu-id="707b8-122">PlaylistLocating</span></span>        | <span data-ttu-id="707b8-123">Windows Media Player versucht, die Wiedergabeliste zu finden.</span><span class="sxs-lookup"><span data-stu-id="707b8-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="707b8-124">Die Wiedergabeliste kann lokal (Bibliothek oder Metadatei mit der Dateinamenerweiterung. ASX) oder Remote sein.</span><span class="sxs-lookup"><span data-stu-id="707b8-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="707b8-125">3</span><span class="sxs-lookup"><span data-stu-id="707b8-125">3</span></span>     | <span data-ttu-id="707b8-126">Playlistconnecting</span><span class="sxs-lookup"><span data-stu-id="707b8-126">PlaylistConnecting</span></span>      | <span data-ttu-id="707b8-127">Verbindung mit der Wiedergabeliste wird hergestellt.</span><span class="sxs-lookup"><span data-stu-id="707b8-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="707b8-128">4</span><span class="sxs-lookup"><span data-stu-id="707b8-128">4</span></span>     | <span data-ttu-id="707b8-129">Playlistload</span><span class="sxs-lookup"><span data-stu-id="707b8-129">PlaylistLoading</span></span>         | <span data-ttu-id="707b8-130">Die Wiedergabeliste wurde gefunden und wird jetzt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="707b8-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="707b8-131">5</span><span class="sxs-lookup"><span data-stu-id="707b8-131">5</span></span>     | <span data-ttu-id="707b8-132">Playlistopening</span><span class="sxs-lookup"><span data-stu-id="707b8-132">PlaylistOpening</span></span>         | <span data-ttu-id="707b8-133">Die Wiedergabeliste wurde abgerufen und nun analysiert und geladen.</span><span class="sxs-lookup"><span data-stu-id="707b8-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="707b8-134">6</span><span class="sxs-lookup"><span data-stu-id="707b8-134">6</span></span>     | <span data-ttu-id="707b8-135">Playlistopennomedia</span><span class="sxs-lookup"><span data-stu-id="707b8-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="707b8-136">Die Wiedergabeliste ist geöffnet.</span><span class="sxs-lookup"><span data-stu-id="707b8-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="707b8-137">7</span><span class="sxs-lookup"><span data-stu-id="707b8-137">7</span></span>     | <span data-ttu-id="707b8-138">Playlistchanged</span><span class="sxs-lookup"><span data-stu-id="707b8-138">PlaylistChanged</span></span>         | <span data-ttu-id="707b8-139">**Currentwiedergabe** wurde eine neue Wiedergabeliste zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="707b8-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="707b8-140">8</span><span class="sxs-lookup"><span data-stu-id="707b8-140">8</span></span>     | <span data-ttu-id="707b8-141">Mediachanging</span><span class="sxs-lookup"><span data-stu-id="707b8-141">MediaChanging</span></span>           | <span data-ttu-id="707b8-142">Ein neues Medien Element soll geladen werden.</span><span class="sxs-lookup"><span data-stu-id="707b8-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="707b8-143">9</span><span class="sxs-lookup"><span data-stu-id="707b8-143">9</span></span>     | <span data-ttu-id="707b8-144">Medialocating</span><span class="sxs-lookup"><span data-stu-id="707b8-144">MediaLocating</span></span>           | <span data-ttu-id="707b8-145">Das Medien Element wird von Windows Media Player gefunden.</span><span class="sxs-lookup"><span data-stu-id="707b8-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="707b8-146">Die Datei kann lokal oder Remote sein.</span><span class="sxs-lookup"><span data-stu-id="707b8-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="707b8-147">10</span><span class="sxs-lookup"><span data-stu-id="707b8-147">10</span></span>    | <span data-ttu-id="707b8-148">Mediaconnecting</span><span class="sxs-lookup"><span data-stu-id="707b8-148">MediaConnecting</span></span>         | <span data-ttu-id="707b8-149">Verbindung mit dem Server, der das Medien Element enthält.</span><span class="sxs-lookup"><span data-stu-id="707b8-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="707b8-150">11</span><span class="sxs-lookup"><span data-stu-id="707b8-150">11</span></span>    | <span data-ttu-id="707b8-151">Medialoading</span><span class="sxs-lookup"><span data-stu-id="707b8-151">MediaLoading</span></span>            | <span data-ttu-id="707b8-152">Das Medien Element wurde gefunden und wird jetzt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="707b8-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="707b8-153">12</span><span class="sxs-lookup"><span data-stu-id="707b8-153">12</span></span>    | <span data-ttu-id="707b8-154">Mediaopening</span><span class="sxs-lookup"><span data-stu-id="707b8-154">MediaOpening</span></span>            | <span data-ttu-id="707b8-155">Das Medien Element wurde abgerufen und wird jetzt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="707b8-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="707b8-156">13</span><span class="sxs-lookup"><span data-stu-id="707b8-156">13</span></span>    | <span data-ttu-id="707b8-157">Mediaopen</span><span class="sxs-lookup"><span data-stu-id="707b8-157">MediaOpen</span></span>               | <span data-ttu-id="707b8-158">Das Medien Element ist jetzt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="707b8-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="707b8-159">14</span><span class="sxs-lookup"><span data-stu-id="707b8-159">14</span></span>    | <span data-ttu-id="707b8-160">Begincodecerwerbs</span><span class="sxs-lookup"><span data-stu-id="707b8-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="707b8-161">Die Codec-Übernahme wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="707b8-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="707b8-162">15</span><span class="sxs-lookup"><span data-stu-id="707b8-162">15</span></span>    | <span data-ttu-id="707b8-163">Endcodecerwerbs</span><span class="sxs-lookup"><span data-stu-id="707b8-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="707b8-164">Die Codec-Erfassung ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="707b8-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="707b8-165">16</span><span class="sxs-lookup"><span data-stu-id="707b8-165">16</span></span>    | <span data-ttu-id="707b8-166">Beginliceneracquisition</span><span class="sxs-lookup"><span data-stu-id="707b8-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="707b8-167">Erwerben einer Lizenz für die Wiedergabe von DRM-geschütztem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="707b8-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="707b8-168">17</span><span class="sxs-lookup"><span data-stu-id="707b8-168">17</span></span>    | <span data-ttu-id="707b8-169">Endliceneracquisition</span><span class="sxs-lookup"><span data-stu-id="707b8-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="707b8-170">Lizenz zum Wiedergeben von DRM-geschütztem Inhalt wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="707b8-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="707b8-171">18</span><span class="sxs-lookup"><span data-stu-id="707b8-171">18</span></span>    | <span data-ttu-id="707b8-172">Beginindividual alization</span><span class="sxs-lookup"><span data-stu-id="707b8-172">BeginIndividualization</span></span>  | <span data-ttu-id="707b8-173">Beginnen Sie mit DRM-Individualisierung.</span><span class="sxs-lookup"><span data-stu-id="707b8-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="707b8-174">19</span><span class="sxs-lookup"><span data-stu-id="707b8-174">19</span></span>    | <span data-ttu-id="707b8-175">Umdindividualization</span><span class="sxs-lookup"><span data-stu-id="707b8-175">EndIndividualization</span></span>    | <span data-ttu-id="707b8-176">Die DRM-Individualisierung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="707b8-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="707b8-177">20</span><span class="sxs-lookup"><span data-stu-id="707b8-177">20</span></span>    | <span data-ttu-id="707b8-178">Mediawaiting</span><span class="sxs-lookup"><span data-stu-id="707b8-178">MediaWaiting</span></span>            | <span data-ttu-id="707b8-179">Es wird auf ein Medien Element gewartet.</span><span class="sxs-lookup"><span data-stu-id="707b8-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="707b8-180">21</span><span class="sxs-lookup"><span data-stu-id="707b8-180">21</span></span>    | <span data-ttu-id="707b8-181">Openingunknownurl</span><span class="sxs-lookup"><span data-stu-id="707b8-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="707b8-182">Öffnen einer URL mit einem unbekannten Typ.</span><span class="sxs-lookup"><span data-stu-id="707b8-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="707b8-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="707b8-183">Remarks</span></span>

<span data-ttu-id="707b8-184">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="707b8-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="707b8-185">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="707b8-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="707b8-186">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="707b8-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="707b8-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="707b8-187">Requirements</span></span>



| <span data-ttu-id="707b8-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="707b8-188">Requirement</span></span> | <span data-ttu-id="707b8-189">Wert</span><span class="sxs-lookup"><span data-stu-id="707b8-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="707b8-190">Version</span><span class="sxs-lookup"><span data-stu-id="707b8-190">Version</span></span><br/> | <span data-ttu-id="707b8-191">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="707b8-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="707b8-192">DLL</span><span class="sxs-lookup"><span data-stu-id="707b8-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="707b8-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707b8-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707b8-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="707b8-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707b8-195">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="707b8-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="707b8-196">**Player. OpenStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="707b8-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





