---
title: Vergleich von detaillierten Objekt Modellen
description: Vergleich von detaillierten Objekt Modellen
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Versions Unterschiede
- Objektmodell, Versions Unterschiede
- Windows Media Player ActiveX-Steuerelement, Versions Unterschiede
- ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile ActiveX-Steuerelement, Versions Unterschiede
- Windows Media Player Mobile, Objektmodell
- Migrations Handbuch, Versions Unterschiede
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038501"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="15346-112">Vergleich von detaillierten Objekt Modellen</span><span class="sxs-lookup"><span data-stu-id="15346-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="15346-113">In der folgenden Tabelle werden die Eigenschaften des Windows Media Player 6,4-Objektmodells mit dem Objektmodell Windows Media Player 7 oder höher verglichen.</span><span class="sxs-lookup"><span data-stu-id="15346-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15346-114">Windows Media Player 6,4-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15346-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="15346-115">Entsprechung für Windows Media Player 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="15346-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15346-116"><em>Player6</em>. <strong>Allowchangedisplaysize</strong></span><span class="sxs-lookup"><span data-stu-id="15346-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="15346-117">Die Anzeige von Windows Media Player 7 oder höher wird automatisch an die Medien angepasst.</span><span class="sxs-lookup"><span data-stu-id="15346-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="15346-118">Sie können die Eigenschaften für Höhe und Breite im- <OBJECT> Tag oder im-Skript festlegen.</span><span class="sxs-lookup"><span data-stu-id="15346-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-119"><em>Player6</em>. <strong>Allowscan</strong></span><span class="sxs-lookup"><span data-stu-id="15346-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="15346-120">-Steuer <em>Elemente</em>.</span><span class="sxs-lookup"><span data-stu-id="15346-120"><em>Controls</em>.</span></span> <span data-ttu-id="15346-121"><strong>FastForward</strong> -und-Steuer <em>Elemente</em>. <strong>fastreverse</strong> sind automatisch für Dateitypen aktiviert, die diese Methoden unterstützen.</span><span class="sxs-lookup"><span data-stu-id="15346-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-122"><em>Player6</em>. <strong>Anglesavailable</strong></span><span class="sxs-lookup"><span data-stu-id="15346-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-123">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-124"><em>Player6</em>. <strong>Animationatstart</strong></span><span class="sxs-lookup"><span data-stu-id="15346-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="15346-125">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-126"><em>Player6</em>. <strong>Audiostream</strong></span><span class="sxs-lookup"><span data-stu-id="15346-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="15346-127">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguageindex</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-128"><em>Player6</em>. <strong>Audiostreamsavailable</strong></span><span class="sxs-lookup"><span data-stu-id="15346-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-129">Verwenden Sie Steuer <em>Elemente</em>. <strong>audiolanguagecount</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-130"><em>Player6</em>. <strong>Autorewind</strong></span><span class="sxs-lookup"><span data-stu-id="15346-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="15346-131">Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong> im Skript, um die aktuelle Position anzugeben oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15346-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="15346-132">Verwenden Sie alternativ Marker und den <em>Player</em>. <strong>markerhit</strong> -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="15346-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-133"><em>Player6</em>. <strong>AutoSize</strong></span><span class="sxs-lookup"><span data-stu-id="15346-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="15346-134">Die automatische Größenanpassung ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="15346-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="15346-135">Wenn Sie die automatische Größenanpassung überschreiben möchten, legen Sie die Eigenschaften Height und Width im- <OBJECT> Tag oder im-Skript fest</span><span class="sxs-lookup"><span data-stu-id="15346-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-136"><em>Player6</em>. <strong>Autostart</strong></span><span class="sxs-lookup"><span data-stu-id="15346-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="15346-137">Verwenden Sie <em>Einstellungen</em>. <strong>Autostart</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-138"><em>Player6</em>. <strong>Saldo</strong></span><span class="sxs-lookup"><span data-stu-id="15346-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="15346-139">Verwenden Sie <em>Einstellungen</em>. <strong>Gleichgewicht</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-140"><em>Player6</em>. <strong>Bandbreite</strong></span><span class="sxs-lookup"><span data-stu-id="15346-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="15346-141"><em>Netzwerk</em>verwenden. <strong>Bandbreite</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-142"><em>Player6</em>. <strong>Baseurl</strong></span><span class="sxs-lookup"><span data-stu-id="15346-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="15346-143">Verwenden Sie <em>Einstellungen</em>. <strong>baseurl</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-144"><em>Player6</em>. <strong>Bufferingcount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="15346-145"><em>Netzwerk verwenden.</em> <strong>bufferingcount</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-146"><em>Player6</em>. <strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="15346-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="15346-147"><em>Netzwerk</em>verwenden. <strong>BufferingProgress</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-148"><em>Player6</em>. <strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="15346-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="15346-149"><em>Netzwerk</em>verwenden. <strong>BufferingTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-150"><em>Player6</em>. <strong>Buttonsavailable</strong></span><span class="sxs-lookup"><span data-stu-id="15346-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-151">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-152"><em>Player6</em>. <strong>Canpreview</strong></span><span class="sxs-lookup"><span data-stu-id="15346-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="15346-153">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-154"><em>Player6</em>. <strong>Canscan</strong></span><span class="sxs-lookup"><span data-stu-id="15346-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="15346-155">Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong>( &quot; FastForward &quot; ) und Steuer <em>Elemente</em>.<strong> IsAvailable</strong>( &quot; fastreverse &quot; ).</span><span class="sxs-lookup"><span data-stu-id="15346-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="15346-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="15346-157">Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong> , um zu testen, ob eine bestimmte Seek-Methode ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="15346-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-158"><em>Player6</em>. <strong>Canseektomarkers</strong></span><span class="sxs-lookup"><span data-stu-id="15346-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="15346-159">Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong>( &quot; currentmarker &quot; ).</span><span class="sxs-lookup"><span data-stu-id="15346-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="15346-160">Verwenden Sie <em>Medien</em>. <strong>markercount</strong> , um die Anzahl von Markern in einem bestimmten Medien Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15346-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="15346-161">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentmarker</strong> zum angeben oder Abrufen der aktuellen Markernummer.</span><span class="sxs-lookup"><span data-stu-id="15346-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-162"><em>Player6</em>. <strong>Captioningid</strong></span><span class="sxs-lookup"><span data-stu-id="15346-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="15346-163">Verwenden Sie <em>closedcaption</em>. <strong>captioningid</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-164"><em>Player6</em>. <strong>Ccactive</strong></span><span class="sxs-lookup"><span data-stu-id="15346-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="15346-165">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-165">Not available.</span></span> <span data-ttu-id="15346-166">Informationen <a href="closed-captioning.md">dazu,</a> wie sich Untertitel in Windows Media Player geändert haben, finden Sie unter Untertitel.</span><span class="sxs-lookup"><span data-stu-id="15346-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-167"><em>Player6</em>. <strong>Channeldescription</strong></span><span class="sxs-lookup"><span data-stu-id="15346-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="15346-168">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-169"><em>Player6</em>. <strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="15346-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="15346-170">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-171"><em>Player6</em>. <strong>Channelurl</strong></span><span class="sxs-lookup"><span data-stu-id="15346-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="15346-172">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-173"><em>Player6</em>. <strong>Clicktoplay</strong></span><span class="sxs-lookup"><span data-stu-id="15346-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="15346-174">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-174">Not available.</span></span> <span data-ttu-id="15346-175">Sie sollten Steuerelemente in der Benutzeroberfläche bereitstellen, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="15346-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="15346-176">Alternativ kann der Benutzer mit der rechten Maustaste auf das Videobild klicken, um ein Popup Menü zu öffnen, das eine <strong>Wiedergabe</strong> -/Unterbrechungs Auswahl bei <em>Player</em>enthält. <strong>enablecontextmenu</strong> ist "true".</span><span class="sxs-lookup"><span data-stu-id="15346-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="15346-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="15346-178">Nicht verfügbar. Mit der Windows Media Player 9-Serie oder höher kann der Benutzer auswählen, ob eine eindeutige Player-ID an Inhaltsanbieter übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="15346-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="15346-179">Wenn der Benutzer diese Option auswählt, sendet der Spieler eine eindeutige ID an den Windows Media-Server.</span><span class="sxs-lookup"><span data-stu-id="15346-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="15346-180">Die ID wird in der Protokolldatei des Servers protokolliert, die sich in der befindet. <em>system32\logfiles unter</em> Ordner standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="15346-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="15346-181">Der Name des Protokoll Felds ist &quot; c-playerid &quot; .</span><span class="sxs-lookup"><span data-stu-id="15346-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="15346-182">Die Server Protokollierung ist in Windows Media Services standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="15346-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="15346-183">Wenn der Benutzer diese Option nicht aktiviert, generiert der Server eine zufällige Sitzungs-ID, die für jeden Client für eine bestimmte Sitzung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="15346-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="15346-184">Weitere Informationen finden Sie in der Dokumentation zu Windows Media Services 9-Serie.</span><span class="sxs-lookup"><span data-stu-id="15346-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-185"><em>Player6</em>. <strong>Codeccount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="15346-186">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-187"><em>Player6</em>. <strong>Colorkey</strong></span><span class="sxs-lookup"><span data-stu-id="15346-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="15346-188">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-189"><em>Player6</em>. <strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="15346-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="15346-190">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-190">Not available.</span></span> <span data-ttu-id="15346-191"><em>Netzwerk</em>verwenden. <strong>Bitrate</strong> zum Bestimmen der aktuellen Bitrate.</span><span class="sxs-lookup"><span data-stu-id="15346-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-192"><em>Player6</em>. <strong>Contactaddress</strong></span><span class="sxs-lookup"><span data-stu-id="15346-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="15346-193">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-194"><em>Player6</em>. <strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="15346-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="15346-195">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-196"><em>Player6</em>. <strong>Contactphone</strong></span><span class="sxs-lookup"><span data-stu-id="15346-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="15346-197">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-198"><em>Player6</em>. " <strong>Erdate</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="15346-199">Verwenden Sie <em>mediacollection</em>. <strong>getmediaatom</strong>(" &quot; &quot; Erstellungsdatum"), um den Index des Erstellungs Datums Atom abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15346-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="15346-200">Verwenden Sie <em>Medien</em>. <strong>getiteminfobyatom</strong> zum Abrufen der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="15346-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-201"><em>Player6</em>. <strong>Currentangle</strong></span><span class="sxs-lookup"><span data-stu-id="15346-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="15346-202">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-203"><em>Player6</em>. <strong>Currentaudiostream</strong></span><span class="sxs-lookup"><span data-stu-id="15346-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="15346-204">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguageindex</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-205"><em>Player6</em>. <strong>Currentbutton</strong></span><span class="sxs-lookup"><span data-stu-id="15346-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="15346-206">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-207"><em>Player6</em>. <strong>Currentccservice</strong></span><span class="sxs-lookup"><span data-stu-id="15346-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="15346-208">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-209"><em>Player6</em>. <strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="15346-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="15346-210">Rufen Sie die aktuelle Wiedergabeliste ab.</span><span class="sxs-lookup"><span data-stu-id="15346-210">Retrieve the current playlist.</span></span> <span data-ttu-id="15346-211">, Wenn die aktuelle Wiedergabeliste nicht die gleiche ist wie die von <em>CDROM</em>zurückgegebene Wiedergabeliste. <strong>Wiedergabeliste</strong>, dann gibt es kein Aktuelles Kapitel.</span><span class="sxs-lookup"><span data-stu-id="15346-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="15346-212">Andernfalls ist die aktuelle Kapitel Nummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="15346-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-213"><em>Player6</em>. <strong>Currentdiscside</strong></span><span class="sxs-lookup"><span data-stu-id="15346-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="15346-214">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="15346-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="15346-216">Verwenden Sie <em>DVD</em>. <strong>Domäne</strong>:</span><span class="sxs-lookup"><span data-stu-id="15346-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-217"><em>Player6</em>. <strong>Currentmarker</strong></span><span class="sxs-lookup"><span data-stu-id="15346-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="15346-218">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentmarker</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="15346-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="15346-220">Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-221"><em>Player6</em>. <strong>Currentsubpicturestream</strong></span><span class="sxs-lookup"><span data-stu-id="15346-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="15346-222">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="15346-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="15346-224">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentPositionTimecode</strong>, Steuer <em>Elemente</em>. <strong>currentpositionstring</strong>, oder-Steuer <em>Elemente</em>. <strong>CurrentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-225"><em>Player6</em>. <strong>Currenttitle</strong></span><span class="sxs-lookup"><span data-stu-id="15346-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="15346-226">Rufen Sie die aktuelle Wiedergabeliste ab.</span><span class="sxs-lookup"><span data-stu-id="15346-226">Retrieve the current playlist.</span></span> <span data-ttu-id="15346-227">, Wenn die aktuelle Wiedergabeliste dieselbe wie die von <em>CDROM</em>zurückgegebene Wiedergabeliste ist. <strong>Wiedergabeliste</strong>, dann ist die Titel Nummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="15346-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-228"><em>Player6</em>. <strong>Currentvolume</strong></span><span class="sxs-lookup"><span data-stu-id="15346-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="15346-229">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-230"><em>Player6</em>. <strong>Cursor Type</strong></span><span class="sxs-lookup"><span data-stu-id="15346-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="15346-231">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-231">Not available.</span></span> <span data-ttu-id="15346-232">Verwenden Sie stattdessen Internet Explorer-Stile.</span><span class="sxs-lookup"><span data-stu-id="15346-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-233"><em>Player6</em>. <strong>Defaultframe</strong></span><span class="sxs-lookup"><span data-stu-id="15346-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="15346-234">Verwenden Sie <em>Einstellungen</em>. <strong>defaultframe</strong>oder Verwenden eines</span><span class="sxs-lookup"><span data-stu-id="15346-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="15346-235">-Attribut im- <OBJECT> Element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="15346-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-236"><em>Player6</em>. <strong>Display BackColor</strong></span><span class="sxs-lookup"><span data-stu-id="15346-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="15346-237">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-238"><em>Player6</em>. <strong>Display ForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="15346-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="15346-239">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="15346-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="15346-241">Die aktuelle Position kann in Sekunden von Anfang an als <strong>Zahl</strong> mithilfe von-Steuer <em>Elementen</em>abgerufen werden. <strong>CurrentPosition</strong>als <strong>Zeichen</strong> Folge, die als hh: mm: SS (Stunden, Minuten, Sekunden) mit Steuer <em>Elementen</em>formatiert ist. <strong>currentpositionstring</strong>oder im Zeit Code Format mithilfe von-Steuer <em>Elementen</em>. <strong>currentPositionTimecode</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-242"><em>Player6</em>. <strong>Display</strong></span><span class="sxs-lookup"><span data-stu-id="15346-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="15346-243">Die Standard Anzeige wird automatisch an die Medien angepasst.</span><span class="sxs-lookup"><span data-stu-id="15346-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="15346-244">Sie können die Eigenschaften für Höhe und Breite im- <OBJECT> Tag oder im Skript festlegen.</span><span class="sxs-lookup"><span data-stu-id="15346-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="15346-245">Verwenden Sie <em>Player</em>. <strong>Vollbild</strong> , um in den Vollbildmodus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="15346-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-246"><em>Player6</em>. <strong>Dauer</strong></span><span class="sxs-lookup"><span data-stu-id="15346-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="15346-247">Verwenden Sie <em>Medien</em>. <strong>Dauer</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-248"><em>Player6</em>. <strong>DVD</strong></span><span class="sxs-lookup"><span data-stu-id="15346-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="15346-249">Verwenden Sie <em>Player</em>. <strong>DVD</strong>:</span><span class="sxs-lookup"><span data-stu-id="15346-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-250"><em>Player6</em>. <strong>Enablecontextmenu</strong></span><span class="sxs-lookup"><span data-stu-id="15346-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="15346-251">Verwenden Sie <em>Player</em>. <strong>enablecontextmenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-252"><em>Player6</em>. <strong>Aktiviert</strong></span><span class="sxs-lookup"><span data-stu-id="15346-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="15346-253">Verwenden Sie <em>Player</em>. <strong>aktiviert</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-254"><em>Player6</em>. <strong>Enablefullscreencontrols</strong></span><span class="sxs-lookup"><span data-stu-id="15346-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="15346-255">Wenn Sie Windows Media Player 9 oder höher verwenden, werden voll Bild Steuerelemente automatisch aktiviert, es sei denn, <em>Player</em>. <strong>uiMode</strong>  =  &quot; keine &quot; .</span><span class="sxs-lookup"><span data-stu-id="15346-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-256"><em>Player6</em>. <strong>Enablepositioncontrols</strong></span><span class="sxs-lookup"><span data-stu-id="15346-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="15346-257">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-257">Not available.</span></span> <span data-ttu-id="15346-258">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-259"><em>Player6</em>. <strong>Enabletracker</strong></span><span class="sxs-lookup"><span data-stu-id="15346-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="15346-260">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-260">Not available.</span></span> <span data-ttu-id="15346-261">Sie können ein benutzerdefiniertes Steuerelement bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-262"><em>Player6</em>. <strong>Entrycount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="15346-263">Verwenden Sie <em>Wiedergabeliste</em>. <strong>Anzahl</strong></span><span class="sxs-lookup"><span data-stu-id="15346-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-264"><em>Player6</em>. <strong>ErrorCode</strong></span><span class="sxs-lookup"><span data-stu-id="15346-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="15346-265">Verwenden Sie <em>ErrorItem</em>. <strong>errorCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-266"><em>Player6</em>. <strong>Errorkorrektur</strong></span><span class="sxs-lookup"><span data-stu-id="15346-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="15346-267">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="15346-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="15346-269">Verwenden Sie <em>ErrorItem</em>. <strong>ErrorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-270"><em>Player6</em>. <strong>Dateiname</strong></span><span class="sxs-lookup"><span data-stu-id="15346-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="15346-271">Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="15346-272">Verwenden Sie Steuer <em>Elemente</em>. ein Ereignis, <strong>das beim Arbeiten</strong> innerhalb einer Wiedergabeliste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15346-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-273"><em>Player6</em>. <strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="15346-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="15346-274">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="15346-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="15346-276"><em>Fehler</em>bei Verwendung. <strong>errorCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-277"><em>Player6</em>. <strong>Hasmultipleitems</strong></span><span class="sxs-lookup"><span data-stu-id="15346-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="15346-278">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-279"><em>Player6</em>. <strong>Imagesourceheight</strong></span><span class="sxs-lookup"><span data-stu-id="15346-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="15346-280">Verwenden Sie <em>Medien</em>. <strong>imagesourceheight</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-281"><em>Player6</em>. <strong>Imagesourcewidth</strong></span><span class="sxs-lookup"><span data-stu-id="15346-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="15346-282">Verwenden Sie <em>Medien</em>. <strong>imagesourcewidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-283"><em>Player6</em>. <strong>Invokeurls</strong></span><span class="sxs-lookup"><span data-stu-id="15346-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="15346-284">Verwenden Sie <em>Einstellungen</em>. <strong>invokeurls</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-285"><em>Player6</em>. <strong>Isbroadcast</strong></span><span class="sxs-lookup"><span data-stu-id="15346-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="15346-286"><em>Netzwerk</em>verwenden. <strong>sourceprotocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-287"><em>Player6</em>. <strong>Isdurationvalid</strong></span><span class="sxs-lookup"><span data-stu-id="15346-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="15346-288">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-288">Not available.</span></span> <span data-ttu-id="15346-289"><em>Medien</em>: die <strong>Dauer</strong> enthält einen gültigen Wert, wenn Sie mit dem aktuellen Medienobjekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15346-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-290"><em>Player6</em>. <strong>Sprache</strong></span><span class="sxs-lookup"><span data-stu-id="15346-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="15346-291">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong></span><span class="sxs-lookup"><span data-stu-id="15346-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-292"><em>Player6</em>. <strong>Lostpakete</strong></span><span class="sxs-lookup"><span data-stu-id="15346-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="15346-293"><em>Netzwerk</em>verwenden. <strong>lostpakete</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-294"><em>Player6</em>. <strong>Markercount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="15346-295">Verwenden Sie <em>Medien</em>. <strong>markercount</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-296"><em>Player6</em>. <strong>Stumm schalten</strong></span><span class="sxs-lookup"><span data-stu-id="15346-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="15346-297">Verwenden Sie <em>Einstellungen</em>. <strong>stumm schalten</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-298"><em>Player6</em>. <strong>Openstate</strong></span><span class="sxs-lookup"><span data-stu-id="15346-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="15346-299">Verwenden Sie <em>Player</em>. <strong>openstate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-300"><em>Player6</em>. <strong>Playcount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="15346-301">Verwenden Sie <em>Einstellungen</em>. <strong>playcount</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-302"><em>Player6</em>. <strong>Playstate</strong></span><span class="sxs-lookup"><span data-stu-id="15346-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="15346-303">Verwenden Sie <em>Player</em>. <strong>playstate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-304"><em>Player6</em>. <strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="15346-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="15346-305">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-305">Not available.</span></span> <span data-ttu-id="15346-306">Verwenden Sie eine Skript Schleifen Struktur mit einem HTML-Timer, um diese Funktionalität zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="15346-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-307"><em>Player6</em>. <strong>Rate</strong></span><span class="sxs-lookup"><span data-stu-id="15346-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="15346-308">Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-309"><em>Player6</em>. Read- <strong>State</strong></span><span class="sxs-lookup"><span data-stu-id="15346-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="15346-310">Verwenden Sie <em>Player</em>. <strong>openstate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-311"><em>Player6</em>. <strong>Receivedpakete</strong></span><span class="sxs-lookup"><span data-stu-id="15346-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="15346-312"><em>Netzwerk</em>verwenden. <strong>receivedpakete</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-313"><em>Player6</em>. " <strong>Receptionquality</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="15346-314"><em>Netzwerk</em>verwenden. " <strong>receptionquality</strong>".</span><span class="sxs-lookup"><span data-stu-id="15346-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-315"><em>Player6</em>. Wieder <strong>herstellbare Pakete</strong></span><span class="sxs-lookup"><span data-stu-id="15346-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="15346-316"><em>Netzwerk</em>verwenden. wieder <strong>herstellbare Pakete</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-317"><em>Player6</em>. <strong></strong> Stamm</span><span class="sxs-lookup"><span data-stu-id="15346-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="15346-318">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-319"><em>Player6</em>. <strong>Samifilename</strong></span><span class="sxs-lookup"><span data-stu-id="15346-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="15346-320">Verwenden Sie <em>closedcaption</em>. <strong>Samifilename</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-321"><em>Player6</em>. <strong>Samilang</strong></span><span class="sxs-lookup"><span data-stu-id="15346-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="15346-322">Verwenden Sie <em>closedcaption</em>. <strong>Samilang</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-323"><em>Player6</em>. <strong>Samistyle</strong></span><span class="sxs-lookup"><span data-stu-id="15346-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="15346-324">Verwenden Sie <em>closedcaption</em>. <strong>Samistyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-325"><em>Player6</em>. <strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="15346-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="15346-326">Verwenden Sie <em>Medien</em>. <strong>Dauer</strong> zur Bestimmung der Länge eines <strong>Medien</strong> Objekts.</span><span class="sxs-lookup"><span data-stu-id="15346-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="15346-327">Verwenden Sie einen Marker mit-Steuer <em>Elementen</em>. <strong>currentmarker</strong> , um eine benutzerdefinierte Endposition anzugeben.</span><span class="sxs-lookup"><span data-stu-id="15346-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-328"><em>Player6</em>. <strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="15346-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="15346-329">Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong> , um die Wiedergabe an einer bestimmten Position zu starten oder einen Marker mit Steuer <em>Elementen</em>zu verwenden. <strong>currentmarker</strong> zum Angeben einer benutzerdefinierten Startposition.</span><span class="sxs-lookup"><span data-stu-id="15346-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-330"><em>Player6</em>. <strong>Senderrorevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="15346-331">Fehler werden in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="15346-331">Errors are queued.</span></span> <span data-ttu-id="15346-332">Verwenden Sie das <strong>Error</strong> -Objekt und das <strong>ErrorItem</strong> -Objekt, um Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15346-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-333"><em>Player6</em>. <strong>Sendkeyboarentvents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="15346-334">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-335"><em>Player6</em>. <strong>Sendmouserclickevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="15346-336">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-337"><em>Player6</em>. <strong>Sendmousermuveevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="15346-338">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-339"><em>Player6</em>. <strong>Sendopenstatechangeevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="15346-340">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-341"><em>Player6</em>. <strong>Sendplaystatechangeevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="15346-342">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-343"><em>Player6</em>. <strong>Sendwarningevents</strong></span><span class="sxs-lookup"><span data-stu-id="15346-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="15346-344">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-345"><em>Player6</em>. <strong>Showaudiocontrols</strong></span><span class="sxs-lookup"><span data-stu-id="15346-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="15346-346">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-346">Not available.</span></span> <span data-ttu-id="15346-347">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-348"><em>Player6</em>. <strong>Show</strong> Titel</span><span class="sxs-lookup"><span data-stu-id="15346-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="15346-349">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-349">Not available.</span></span> <span data-ttu-id="15346-350">Sie können eine benutzerdefinierte geschlossene Beschriftungs Anzeige angeben.</span><span class="sxs-lookup"><span data-stu-id="15346-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-351"><em>Player6</em>. <strong>ShowControls</strong></span><span class="sxs-lookup"><span data-stu-id="15346-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="15346-352">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-352">Not available.</span></span> <span data-ttu-id="15346-353">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-354"><em>Player6</em>. <strong>Show Display</strong></span><span class="sxs-lookup"><span data-stu-id="15346-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="15346-355">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-356"><em>Player6</em>. <strong>Showgoinfo-Leiste</strong></span><span class="sxs-lookup"><span data-stu-id="15346-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="15346-357">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-357">Not available.</span></span> <span data-ttu-id="15346-358">Sie können benutzerdefinierte Funktionen mit dem Medienobjekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15346-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-359"><em>Player6</em>. <strong>Showpositioncontrols</strong></span><span class="sxs-lookup"><span data-stu-id="15346-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="15346-360">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-360">Not available.</span></span> <span data-ttu-id="15346-361">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-362"><em>Player6</em>. <strong>ShowStatusBar</strong></span><span class="sxs-lookup"><span data-stu-id="15346-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="15346-363">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-363">Not available.</span></span> <span data-ttu-id="15346-364">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-365"><em>Player6</em>. <strong>Showtracker</strong></span><span class="sxs-lookup"><span data-stu-id="15346-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="15346-366">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-366">Not available.</span></span> <span data-ttu-id="15346-367">Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="15346-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-368"><em>Player6</em>. <strong>Sourcelink</strong></span><span class="sxs-lookup"><span data-stu-id="15346-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="15346-369">Verwenden Sie <em>Medien</em>. <strong>SourceUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-370"><em>Player6</em>. <strong>Sourceprotocol</strong></span><span class="sxs-lookup"><span data-stu-id="15346-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="15346-371"><em>Netzwerk</em>verwenden. <strong>sourceprotocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-372"><em>Player6</em>. <strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="15346-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="15346-373">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-373">Not available.</span></span> <span data-ttu-id="15346-374">Verwenden Sie Steuer <em>Elemente</em>. <strong>audiolanguagecount</strong> zum Abrufen der Anzahl der audiosprachstreams.</span><span class="sxs-lookup"><span data-stu-id="15346-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-375"><em>Player6</em>. <strong>Subpictureon</strong></span><span class="sxs-lookup"><span data-stu-id="15346-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="15346-376">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-377"><em>Player6</em>. <strong>Subpicturestreamsavailable</strong></span><span class="sxs-lookup"><span data-stu-id="15346-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-378">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="15346-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-379"><em>Player6</em>. <strong>Titlesavailable</strong></span><span class="sxs-lookup"><span data-stu-id="15346-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-380">Verwenden Sie Folgendes:<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="15346-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-381"><em>Player6</em>. <strong>Totaltitletime</strong></span><span class="sxs-lookup"><span data-stu-id="15346-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="15346-382">Verwenden Sie <em>currentMedia</em>. <strong>Dauer</strong> oder <em>currentMedia</em>. <strong>durationString</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-383"><em>Player6</em>. <strong>Transparentatstart</strong></span><span class="sxs-lookup"><span data-stu-id="15346-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="15346-384">Verwenden Sie Skripts, um die Höhen-und Breitenwerte anzugeben, um den Player sichtbar oder unsichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="15346-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-385"><em>Player6</em>. <strong>UniqueId</strong></span><span class="sxs-lookup"><span data-stu-id="15346-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="15346-386">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="15346-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="15346-388">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-389"><em>Player6</em>. <strong>Videobordercolor</strong></span><span class="sxs-lookup"><span data-stu-id="15346-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="15346-390">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-391"><em>Player6</em>. <strong>Videoborderwidth</strong></span><span class="sxs-lookup"><span data-stu-id="15346-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="15346-392">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-393"><em>Player6</em>. <strong>Volume</strong></span><span class="sxs-lookup"><span data-stu-id="15346-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="15346-394">Verwenden Sie <em>Einstellungen</em>. <strong>Volume</strong>:</span><span class="sxs-lookup"><span data-stu-id="15346-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-395"><em>Player6</em>. <strong>Volumesesverfügbar</strong></span><span class="sxs-lookup"><span data-stu-id="15346-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="15346-396">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15346-397">In der folgenden Tabelle werden die Objektmodell Methoden von Windows Media Player, Version 6,4, mit dem Objektmodell Windows Media Player 7 oder höher verglichen.</span><span class="sxs-lookup"><span data-stu-id="15346-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15346-398">Windows Media Player 6,4-Methode</span><span class="sxs-lookup"><span data-stu-id="15346-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="15346-399">Entsprechung für Windows Media Player 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="15346-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15346-400"><em>Player6</em>. <strong>Abgangsbox</strong></span><span class="sxs-lookup"><span data-stu-id="15346-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="15346-401">Verwenden Sie <em>Player</em>. <strong>VERSIONINFO</strong> zum Abrufen der Windows-Version Media Player.</span><span class="sxs-lookup"><span data-stu-id="15346-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-402"><em>Player6</em>. <strong>Backwardscan</strong></span><span class="sxs-lookup"><span data-stu-id="15346-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="15346-403">Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-404"><em>Player6</em>. <strong>Buttonaktivierung</strong></span><span class="sxs-lookup"><span data-stu-id="15346-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="15346-405">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-406"><em>Player6</em>. <strong>Buttonselectandaktivierungs</strong></span><span class="sxs-lookup"><span data-stu-id="15346-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="15346-407">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-408"><em>Player6</em>. <strong>Abbrechen</strong></span><span class="sxs-lookup"><span data-stu-id="15346-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="15346-409">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-410"><em>Player6</em>. " <strong>Chapterplay</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="15346-411">Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="15346-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="15346-412">Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.</span><span class="sxs-lookup"><span data-stu-id="15346-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-413"><em>Player6</em>. " <strong>Chapterplayautostoppt</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="15346-414">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-415"><em>Player6</em>. " <strong>Chaptersearch</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="15346-416">Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="15346-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="15346-417">Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.</span><span class="sxs-lookup"><span data-stu-id="15346-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-418"><em>Player6</em>. <strong>FastForward</strong></span><span class="sxs-lookup"><span data-stu-id="15346-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="15346-419">Verwenden Sie Steuer <em>Elemente</em>. <strong>FastForward</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-420"><em>Player6</em>. <strong>Fastreverse</strong></span><span class="sxs-lookup"><span data-stu-id="15346-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="15346-421">Verwenden Sie Steuer <em>Elemente</em>. <strong>fastreverse</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-422"><em>Player6</em>. <strong>Forwardscan</strong></span><span class="sxs-lookup"><span data-stu-id="15346-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="15346-423">Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-424"><em>Player6</em>. <strong>Getallgprms</strong></span><span class="sxs-lookup"><span data-stu-id="15346-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="15346-425">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-426"><em>Player6</em>. <strong>Getallsprms</strong></span><span class="sxs-lookup"><span data-stu-id="15346-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="15346-427">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-428"><em>Player6</em>. <strong>Getaudiolanguage</strong></span><span class="sxs-lookup"><span data-stu-id="15346-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="15346-429">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong> zum Abrufen der LCID der aktuellen Audiosprache.</span><span class="sxs-lookup"><span data-stu-id="15346-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-430"><em>Player6</em>. <strong>Getcodecdescription</strong></span><span class="sxs-lookup"><span data-stu-id="15346-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="15346-431">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-432"><em>Player6</em>. <strong>Getcodecinstallation</strong></span><span class="sxs-lookup"><span data-stu-id="15346-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="15346-433">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-434"><em>Player6</em>. <strong>Getcodecurl</strong></span><span class="sxs-lookup"><span data-stu-id="15346-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="15346-435">Verwenden Sie <em>ErrorItem</em>. <strong>CustomURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-436"><em>Player6</em>. <strong>Getcurrententry</strong></span><span class="sxs-lookup"><span data-stu-id="15346-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="15346-437">Verwenden Sie das Skript zum Durchlaufen der aktuellen Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="15346-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="15346-438">Verwenden Sie <em>Medien</em>. <strong>isidentical</strong> zum Vergleichen der einzelnen Einträge in der Wiedergabeliste mit dem <em>Player</em>. <strong>currentMedia</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="15346-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-439"><em>Player6</em>. <strong>Getmarkername</strong></span><span class="sxs-lookup"><span data-stu-id="15346-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="15346-440">Verwenden Sie <em>Medien</em>. <strong>getmarkername</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-441"><em>Player6</em>. <strong>Getmarkertime</strong></span><span class="sxs-lookup"><span data-stu-id="15346-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="15346-442">Verwenden Sie <em>Medien</em>. <strong>getmarkertime</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-443"><em>Player6</em>. <strong>Getmediainfostring</strong></span><span class="sxs-lookup"><span data-stu-id="15346-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="15346-444">Verwenden Sie <em>Medien</em>. <strong>getiteminfo</strong>, <em>Medium</em>. <strong>getiteminfobyatom</strong>und die zugehörigen Methoden zum Abrufen von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="15346-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-445"><em>Player6</em>. <strong>Getmediaparameter</strong></span><span class="sxs-lookup"><span data-stu-id="15346-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="15346-446">Verwenden Sie <em>Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="15346-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="15346-447">Verwenden Sie dann die- <em>Medien</em>. <strong>getiteminfo</strong> zum Abrufen der Parameter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15346-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-448"><em>Player6</em>. <strong>Getmediaparametername</strong></span><span class="sxs-lookup"><span data-stu-id="15346-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="15346-449">Verwenden Sie <em>Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="15346-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="15346-450">Verwenden Sie dann die- <em>Medien</em>. <strong>GetAttributeName</strong> zum Abrufen der Parameter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="15346-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-451"><em>Player6</em>. <strong>Getmoreingefourl</strong></span><span class="sxs-lookup"><span data-stu-id="15346-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="15346-452">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-453"><em>Player6</em>. <strong>Getnumofchapters</strong></span><span class="sxs-lookup"><span data-stu-id="15346-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="15346-454">Wenn gerade ein Titel wiedergegeben wird, verwenden Sie <em>currentwiedergabe</em>. <strong>Anzahl</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-455"><em>Player6</em>. <strong>Getstreamgroup</strong></span><span class="sxs-lookup"><span data-stu-id="15346-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="15346-456">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-457"><em>Player6</em>. <strong>GetStreamName</strong></span><span class="sxs-lookup"><span data-stu-id="15346-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="15346-458">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-459"><em>Player6</em>. <strong>Getstreamselected</strong></span><span class="sxs-lookup"><span data-stu-id="15346-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="15346-460">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-461"><em>Player6</em>. <strong>Getsubpicturelanguage</strong></span><span class="sxs-lookup"><span data-stu-id="15346-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="15346-462">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-463"><em>Player6</em>. <strong>Goup</strong></span><span class="sxs-lookup"><span data-stu-id="15346-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="15346-464">Verwenden Sie <em>DVD</em>. <strong>zurück</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-465"><em>Player6</em>. <strong>Issoundcardenabled</strong></span><span class="sxs-lookup"><span data-stu-id="15346-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="15346-466">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-467"><em>Player6</em>. <strong>Leftbuttonselect</strong></span><span class="sxs-lookup"><span data-stu-id="15346-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="15346-468">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-469"><em>Player6</em>. <strong>Lowerbuttonselect</strong></span><span class="sxs-lookup"><span data-stu-id="15346-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="15346-470">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-471"><em>Player6</em>. <strong>Menucall</strong></span><span class="sxs-lookup"><span data-stu-id="15346-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="15346-472">Verwenden Sie <em>DVD</em>. <strong>titlemenu</strong> oder <em>DVD</em>. <strong>topmenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-473"><em>Player6</em>. <strong>Nächste</strong></span><span class="sxs-lookup"><span data-stu-id="15346-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="15346-474">Verwenden Sie Steuer <em>Elemente</em>. <strong>als nächstes</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-475"><em>Player6</em>. <strong>Nextpgsearch</strong></span><span class="sxs-lookup"><span data-stu-id="15346-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="15346-476">Verwenden Sie Steuer <em>Elemente</em>. <strong>als nächstes</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-477"><em>Player6</em>. <strong>Öffnen</strong> Sie</span><span class="sxs-lookup"><span data-stu-id="15346-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="15346-478">Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="15346-479">Dateien werden immer asynchron geöffnet.</span><span class="sxs-lookup"><span data-stu-id="15346-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-480"><em>Player6</em>. <strong></strong> Anhalten</span><span class="sxs-lookup"><span data-stu-id="15346-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="15346-481">Verwenden Sie Steuer <em>Elemente</em>. <strong></strong>anhalten.</span><span class="sxs-lookup"><span data-stu-id="15346-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-482"><em>Player6</em>. <strong></strong> Wiedergeben</span><span class="sxs-lookup"><span data-stu-id="15346-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="15346-483">Verwenden Sie Steuer <em>Elemente</em>. wieder <strong>geben.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-484"><em>Player6</em>. <strong>Vorheriges</strong></span><span class="sxs-lookup"><span data-stu-id="15346-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="15346-485">Verwenden Sie Steuer <em>Elemente</em>. <strong>Vorheriges</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-486"><em>Player6</em>. <strong>Prevpgsearch</strong></span><span class="sxs-lookup"><span data-stu-id="15346-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="15346-487">Verwenden Sie Steuer <em>Elemente</em>. <strong>Vorheriges</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-488"><em>Player6</em>. <strong>Resumefrommenu</strong></span><span class="sxs-lookup"><span data-stu-id="15346-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="15346-489">Verwenden Sie <em>DVD</em>. fort <strong>setzen.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-490"><em>Player6</em>. <strong>Rightbuttonselect</strong></span><span class="sxs-lookup"><span data-stu-id="15346-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="15346-491">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-492"><em>Player6</em>. <strong>Setcurrententry</strong></span><span class="sxs-lookup"><span data-stu-id="15346-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="15346-493">Rufen Sie mithilfe von <em>currentwiedergabe</em>ein Medienobjekt ab. <strong>Item</strong>(<em>entrynumber</em>).</span><span class="sxs-lookup"><span data-stu-id="15346-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="15346-494">Geben Sie dann das abgerufene Medienobjekt mithilfe von Steuer <em>Elementen</em>an. der- <strong>Typ.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-495"><em>Player6</em>. <strong>Show Dialog</strong></span><span class="sxs-lookup"><span data-stu-id="15346-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="15346-496">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-497"><em>Player6</em>. <strong>Stilloff</strong></span><span class="sxs-lookup"><span data-stu-id="15346-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="15346-498">Verwenden Sie Steuer <em>Elemente</em>. wieder <strong>geben.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="15346-499">Verwenden Sie alternativ Steuer <em>Elemente</em>. <strong>Als nächstes</strong> , wenn sich derzeit im immer noch Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="15346-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-500"><em>Player6</em>. Wird <strong>beendet</strong></span><span class="sxs-lookup"><span data-stu-id="15346-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="15346-501">Verwenden Sie Steuer <em>Elemente</em>. <strong>beendet</strong>wird.</span><span class="sxs-lookup"><span data-stu-id="15346-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-502"><em>Player6</em>. <strong>Streamselect</strong></span><span class="sxs-lookup"><span data-stu-id="15346-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="15346-503">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-503">Not available.</span></span> <span data-ttu-id="15346-504">Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong> zur Angabe eines audiosprachstreams.</span><span class="sxs-lookup"><span data-stu-id="15346-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-505"><em>Player6</em>. <strong>Timeplay</strong></span><span class="sxs-lookup"><span data-stu-id="15346-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="15346-506">Verwenden Sie in der Stamm Wiedergabeliste <em>currentwiedergabe</em>. <strong>Element</strong>(<em>Index</em>) zum Abrufen eines Medien Objekts.</span><span class="sxs-lookup"><span data-stu-id="15346-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="15346-507">Legen Sie dann das Medienobjekt mithilfe von-Steuer <em>Elementen</em>als Aktuelles fest. der- <strong>Typ.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="15346-508">Geben Sie dann Steuer <em>Elemente</em>an. <strong>CurrentPosition</strong> mit einem Uhrzeitwert in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="15346-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-509"><em>Player6</em>. <strong>Timesearch</strong></span><span class="sxs-lookup"><span data-stu-id="15346-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="15346-510">Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="15346-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-511"><em>Player6</em>. <strong>Titleplay</strong></span><span class="sxs-lookup"><span data-stu-id="15346-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="15346-512">Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="15346-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="15346-513">Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.</span><span class="sxs-lookup"><span data-stu-id="15346-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="15346-514">Verwenden Sie alternativ <em>currentwiedergabe</em>. <strong>Element</strong> zum Abrufen eines Medien Objekts, und verwenden Sie dann das zurückgegebene Medienobjekt, um Steuer <em>Elemente</em>anzugeben. der- <strong>Typ.</strong></span><span class="sxs-lookup"><span data-stu-id="15346-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-515"><em>Player6</em>. " <strong>Toppgsearch</strong> "</span><span class="sxs-lookup"><span data-stu-id="15346-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="15346-516">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15346-517"><em>Player6</em>. <strong>Uopvalid</strong></span><span class="sxs-lookup"><span data-stu-id="15346-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="15346-518">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="15346-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15346-519"><em>Player6</em>. <strong>Upperbuttonselect</strong></span><span class="sxs-lookup"><span data-stu-id="15346-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="15346-520">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15346-521">In der folgenden Tabelle werden die Objektmodell Ereignisse von Windows Media Player, Version 6,4, mit dem Objektmodell Windows Media Player 7 oder höher verglichen.</span><span class="sxs-lookup"><span data-stu-id="15346-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="15346-522">Windows Media Player 6,4-Ereignis</span><span class="sxs-lookup"><span data-stu-id="15346-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="15346-523">Entsprechung für Windows Media Player 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="15346-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15346-524">*Player6*. **Pufferung**</span><span class="sxs-lookup"><span data-stu-id="15346-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="15346-525">Verwenden Sie *Player*. **Pufferung**.</span><span class="sxs-lookup"><span data-stu-id="15346-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="15346-526">*Player6*. **Klicken Sie auf**</span><span class="sxs-lookup"><span data-stu-id="15346-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="15346-527">Verwenden Sie *Player*. **Klicken Sie auf**</span><span class="sxs-lookup"><span data-stu-id="15346-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="15346-528">*Player6*. **DblClick**</span><span class="sxs-lookup"><span data-stu-id="15346-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="15346-529">Verwenden Sie *Player*. **Doppelklick**</span><span class="sxs-lookup"><span data-stu-id="15346-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="15346-530">*Player6*. Verbindung **trennen**</span><span class="sxs-lookup"><span data-stu-id="15346-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="15346-531">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="15346-532">*Player6*. **Displaymodechange**</span><span class="sxs-lookup"><span data-stu-id="15346-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="15346-533">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="15346-534">*Player6*. **Dvdnotify**</span><span class="sxs-lookup"><span data-stu-id="15346-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="15346-535">*Player*. **Domainchange** und *Player*. **Openplaylistswitch** sind DVD-spezifische Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="15346-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="15346-536">Abhängig von der Anwendung können auch andere Ereignisse in Zusammenhang mit Wiedergabe-, Medien-und CD-ROM-Medien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="15346-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="15346-537">*Player6*. **EndOf-Stream**</span><span class="sxs-lookup"><span data-stu-id="15346-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="15346-538">Verwenden Sie *Player*. **Playstate**.</span><span class="sxs-lookup"><span data-stu-id="15346-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="15346-539">*Player6*. **Fehler**</span><span class="sxs-lookup"><span data-stu-id="15346-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="15346-540">Das Ereignis ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="15346-540">The event is unchanged.</span></span> <span data-ttu-id="15346-541">Fehler werden jedoch in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="15346-541">Errors, however, are queued.</span></span> <span data-ttu-id="15346-542">Verwenden Sie das **Error** -Objekt mit dem **ErrorItem** -Objekt, um Fehlerinformationen aus der Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15346-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="15346-543">Sehen Sie sich den Beispielcode im vorherigen Abschnitt Fehlerbehandlung an.</span><span class="sxs-lookup"><span data-stu-id="15346-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="15346-544">*Player6*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="15346-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="15346-545">Verwenden Sie *Player*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="15346-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="15346-546">*Player6*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="15346-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="15346-547">Verwenden Sie *Player*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="15346-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="15346-548">*Player6*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="15346-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="15346-549">Verwenden Sie *Player*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="15346-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="15346-550">*Player6*. **Markerhit**</span><span class="sxs-lookup"><span data-stu-id="15346-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="15346-551">Verwenden Sie *Player*. **Markerhit**.</span><span class="sxs-lookup"><span data-stu-id="15346-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="15346-552">*Player6*. **Mouum**</span><span class="sxs-lookup"><span data-stu-id="15346-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="15346-553">Verwenden Sie *Player*. **Mouum**</span><span class="sxs-lookup"><span data-stu-id="15346-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="15346-554">*Player6*. **Mouseelmove**</span><span class="sxs-lookup"><span data-stu-id="15346-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="15346-555">Verwenden Sie *Player*. **Mouseelmove**</span><span class="sxs-lookup"><span data-stu-id="15346-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="15346-556">*Player6*. **Mouberup**</span><span class="sxs-lookup"><span data-stu-id="15346-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="15346-557">Verwenden Sie *Player*. **Mouberup**</span><span class="sxs-lookup"><span data-stu-id="15346-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="15346-558">*Player6*. **NewStream**</span><span class="sxs-lookup"><span data-stu-id="15346-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="15346-559">Verwenden Sie *Player*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="15346-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="15346-560">*Player6*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="15346-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="15346-561">Verwenden Sie *Player*. **OpenStateChange**.</span><span class="sxs-lookup"><span data-stu-id="15346-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="15346-562">*Player6*. **PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="15346-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="15346-563">Verwenden Sie *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="15346-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="15346-564">*Player6*. **Positionsänderung**</span><span class="sxs-lookup"><span data-stu-id="15346-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="15346-565">Verwenden Sie *Player*. **Positionsänderung**.</span><span class="sxs-lookup"><span data-stu-id="15346-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="15346-566">*Player6*. " **Leserystatechange** "</span><span class="sxs-lookup"><span data-stu-id="15346-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="15346-567">Verwenden Sie *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="15346-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="15346-568">*Player6*. **ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="15346-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="15346-569">Verwenden Sie *Player*. **ScriptCommand**.</span><span class="sxs-lookup"><span data-stu-id="15346-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="15346-570">*Player6*. **Warnung**</span><span class="sxs-lookup"><span data-stu-id="15346-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="15346-571">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15346-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="15346-572">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15346-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15346-573">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="15346-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="15346-574">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="15346-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





