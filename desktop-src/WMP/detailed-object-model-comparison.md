---
title: Detaillierter Objektmodellvergleich
description: Detaillierter Objektmodellvergleich
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player,Objektmodell
- Windows Media Player-Objektmodell, Versionsunterschiede
- Objektmodell, Versionsunterschiede
- Windows Media Player ActiveX,Versionsunterschiede
- ActiveX,Versionsunterschiede
- Windows Media Player Mobile ActiveX-Steuerelement,Versionsunterschiede
- Windows Media Player Mobil, Objektmodell
- Migrationshandbuch, Versionsunterschiede
- Versionen von Windows Media Player,Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f2e092f7e32b889056841b5802dffa141c0be4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884768"
---
# <a name="detailed-object-model-comparison"></a>Detaillierter Objektmodellvergleich

In der folgenden Tabelle werden die Windows Media Player 6.4-Objektmodelleigenschaften mit dem Windows Media Player 7- oder höher-Objektmodell verglichen.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4-Eigenschaft</th>
<th>Windows Media Player 7 oder höher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>Die Anzeige von Windows Media Player 7 oder höher wird automatisch an die Mediengröße geändert. Sie können die Eigenschaften für Höhe und Breite im &lt; &gt; OBJECT-Tag oder im Skript festlegen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Steuert</em>. <strong>fastForward und</strong> <em>Controls</em>. <strong>fastReverse wird</strong> automatisch für Dateitypen aktiviert, die diese Methoden unterstützen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AnglesAvailable</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoRewind</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentPosition</strong> im Skript, um die aktuelle Position anzugeben oder abzurufen. Alternativ können Sie Marker und den <em>Player verwenden.</em> <strong>markerHit-Ereignis.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AutoSize</strong></td>
<td>Die automatische Größeneinstellung ist das Standardverhalten. Um die automatische Größeneinstellung zu überschreiben, legen Sie die Eigenschaften für Höhe und Breite im &lt; &gt; OBJECT-Tag oder im Skript fest.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoStart</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>autoStart</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>ausgleichen.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Bandbreite</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>bandWidth</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Verwenden Sie <em>Netzwerk.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Schaltflächen Verfügbar</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>isAvailable</strong>( &quot; FastForward &quot; ) und <em>Steuert</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>isAvailable,</strong> um zu testen, ob eine bestimmte Suchmethode ausgeführt werden kann.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ). Verwenden Sie <em>Media</em>. <strong>markerCount</strong> zum Abrufen der Anzahl von Markern in einem bestimmten Medienelement. Verwenden Sie <em>Steuerelemente.</em> <strong>currentMarker zum</strong> Angeben oder Abrufen der aktuellen Markernummer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Verwenden <em>Sie ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Nicht verfügbar. Unter <a href="closed-captioning.md">Untertitel finden Sie</a> Informationen dazu, wie sich Untertitel in der Windows Media Player.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>Nicht verfügbar. Sie sollten Steuerelemente in Ihrer Benutzeroberfläche bereitstellen, um die Wiedergabe zu starten. Alternativ kann der Benutzer mit der rechten Maustaste auf das Videobild klicken, um ein Popupmenü zu öffnen, das eine <strong>Wiedergabe-/Pause-Auswahl</strong> enthält, wenn <em>Player</em>. <strong>enableContextMenu</strong> ist gleich TRUE.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Nicht verfügbar. Windows Media Player 9-Serie oder höher kann der Benutzer auswählen, ob eine eindeutige Player-ID an Inhaltsanbieter übertragen wird.<br/> Wenn der Benutzer diese Option auswählt, sendet der Player eine eindeutige ID an den Windows Medienserver. Die ID wird in der Protokolldatei des Servers protokolliert, die sich in der befindet. <em>Der Ordner system32\logfiles</em> ist standardmäßig. Der Name des Protokollfelds ist &quot; c-playerid. &quot; Die Serverprotokollierung ist in der Standardeinstellung nicht Windows Media-Dienste.<br/> Wenn der Benutzer diese Option nicht auswählt, generiert der Server eine zufällige Sitzungs-ID, die für jeden Client für eine bestimmte Sitzung eindeutig ist.<br/> Weitere Informationen finden Sie in der Dokumentation Windows Media-Dienste 9-Serie.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Nicht verfügbar. Verwenden Sie <em>Netzwerk</em>. <strong>bitRate,</strong> um die aktuelle Bitrate zu bestimmen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactAddress</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactPhone</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Verwenden <em>Sie MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ), um den Index des Atoms für das Erstellungsdatum abzurufen. Verwenden Sie <em>Media</em>. <strong>getItemInfoByAtom zum</strong> Abrufen der Metadaten.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentButton</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentCCService</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Rufen Sie die aktuelle Wiedergabeliste ab. Wenn die aktuelle Wiedergabeliste nicht mit der Wiedergabeliste identisch ist, die von <em>Cyan</em>zurückgegeben wird. <strong>Wiedergabeliste</strong>, dann gibt es kein aktuelles Kapitel. Andernfalls ist die aktuelle Kapitelnummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>Domäne</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentPositionTimeCode</strong>, <em>Steuert</em>. <strong>currentPositionString</strong>oder <em>Steuert</em>. <strong>currentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Rufen Sie die aktuelle Wiedergabeliste ab. Wenn die aktuelle Wiedergabeliste mit der wiedergabeliste identisch ist, die von <em>Cyan</em>zurückgegeben wird. <strong>Wiedergabeliste,</strong>dann ist die Titelnummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>Nicht verfügbar. Verwenden Sie stattdessen Internet Explorer Stile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>defaultFrame</strong>, oder verwenden Sie eine <PARAM> -Attribut im &lt; &gt; OBJECT-Element:
<pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayBackColor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplayForeColor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>Die aktuelle Position kann mithilfe von <em>-Steuerelementen</em>in Sekunden vom Anfang als <strong>Zahl</strong> abgerufen werden. <strong>currentPosition</strong>als <strong>Zeichenfolge</strong> im Format HH:MM:SS (Stunden, Minuten, Sekunden) mithilfe von <em>Steuerelementen</em>. <strong>currentPositionString</strong>oder im Zeitcodeformat mithilfe von <em>Controls</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplaySize</strong></td>
<td>Die Größe der Standardanzeige wird automatisch an die Medien angepasst. Sie können die Höhen- und Breiteneigenschaften im &lt; &gt; OBJECT-Tag oder im Skript festlegen. Verwenden Sie <em>Player</em>. <strong>fullScreen</strong> zum Wechseln in den Vollbildmodus.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Dauer</strong></td>
<td>Verwenden Sie <em>Medien.</em> <strong>duration</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Aktiviert</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>aktiviert.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Bei Verwendung Windows Media Player 9er Serie oder höher werden Vollbildsteuerelemente automatisch aktiviert, es sei <em>denn, Player</em>. <strong>uiMode</strong>  =  &quot; none &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uimode,</strong> um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Nicht verfügbar. Sie können ein benutzerdefiniertes Steuerelement bereitstellen oder <em>Player</em>verwenden. <strong>uimode,</strong> um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Verwenden Sie <em>Wiedergabeliste</em>. <strong>count</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Verwenden Sie <em>ErrorItem.</em> <strong>errorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Verwenden Sie <em>ErrorItem.</em> <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FileName</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>. Verwenden Sie <em>Steuerelemente.</em> <strong>currentItem</strong> beim Arbeiten innerhalb einer Wiedergabeliste.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Verwenden Sie <em>den Fehler</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Verwenden Sie <em>Medien.</em> <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Verwenden Sie <em>Medien.</em> <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Verwenden Sie <em>Network</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Nicht verfügbar. <em>Medien</em>. <strong>duration</strong> enthält bei Verwendung mit dem aktuellen Medienobjekt einen gültigen Wert.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sprache</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Verwenden Sie <em>Network</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Verwenden Sie <em>Medien.</em> <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Stummschalten</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>stummschalten.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>playState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Nicht verfügbar. Verwenden Sie eine Skriptschleifenstruktur mit einem HTML-Timer, um diese Funktionalität zu duplizieren.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Rate</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Root</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Verwenden <em>Sie ClosedCaption</em>. <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Verwenden <em>Sie ClosedCaption</em>. <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Verwenden <em>Sie ClosedCaption</em>. <strong>SAMIStyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Verwenden Sie <em>Media</em>. <strong>duration,</strong> um die Länge eines <strong>Medienobjekts zu</strong> bestimmen. Verwenden Sie einen Marker mit <em>Controls</em>. <strong>currentMarker zum</strong> Angeben einer benutzerdefinierten Endposition.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentPosition,</strong> um die Wiedergabe von einer bestimmten Position aus zu starten oder einen Marker mit <em>Controls zu verwenden.</em> <strong>currentMarker zum</strong> Angeben einer benutzerdefinierten Startposition.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Fehler werden in die Warteschlange gestellt. Verwenden Sie <strong>das Error-Objekt</strong> und das <strong>ErrorItem-Objekt,</strong> um Fehlerinformationen abzurufen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendKeyboardEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendMouseClickEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendMouseMoveEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendWarningEvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowAudioControls</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player verwenden.</em> <strong>uimode,</strong> um eine Standardkonfiguration zu wählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>Nicht verfügbar. Sie können eine benutzerdefinierte Untertitelanzeige bereitstellen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player verwenden.</em> <strong>uimode,</strong> um eine Standardkonfiguration zu wählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Funktionen mithilfe des Medienobjekts bereitstellen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player verwenden.</em> <strong>uimode,</strong> um eine Standardkonfiguration zu wählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player verwenden.</em> <strong>uimode,</strong> um eine Standardkonfiguration zu wählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player verwenden.</em> <strong>uimode,</strong> um eine Standardkonfiguration zu wählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Verwenden Sie <em>Media</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Verwenden Sie <em>Netzwerk</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Nicht verfügbar. Verwenden Sie <em>Steuerelemente.</em> <strong>audioLanguageCount zum</strong> Abrufen der Anzahl von Audiosprachstreams.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SubpictureOn</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Verwenden Sie Folgendes:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Verwenden <em>Sie currentMedia</em>. <strong>duration</strong> oder <em>currentMedia</em>. <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Geben Sie mithilfe eines Skripts die Werte für Höhe und Breite an, um den Player sichtbar oder unsichtbar zu machen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>VideoBorderColor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorderWidth</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volume</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>Nicht verfügbar.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Windows Media Player Version 6.4 des Objektmodells mit dem objektmodell Windows Media Player 7 oder höher verglichen.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4-Methode</th>
<th>Windows Media Player 7 oder höher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>versionInfo</strong> zum Abrufen der Version Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ButtonActivate</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abbrechen</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterPlay</strong></td>
<td>Wenn die angegebene Titelwiedergabeliste bereits abspielt, rufen Sie das gewünschte Kapitel mithilfe der folgenden Syntax als Medienobjekt ab:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie dann <em>Player an.</em> <strong>currentMedia unter</strong> Verwendung des zurückgegebenen Medienobjekts.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>KapitelPlayAutoStop</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Wenn die angegebene Titelwiedergabeliste bereits abspielt, rufen Sie das gewünschte Kapitel mithilfe der folgenden Syntax als Medienobjekt ab:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie dann <em>Player an.</em> <strong>currentMedia unter</strong> Verwendung des zurückgegebenen Medienobjekts.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Verwenden <em>Einstellungen</em>. <strong>rate</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAllGPRMs</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetAllSPRMs</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAudioLanguage</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentAudioLanguage</strong> zum Abrufen der LCID der aktuellen Audiosprache.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecDescription</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCodecInstalled</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecURL</strong></td>
<td>Verwenden <em>Sie ErrorItem</em>. <strong>customUrl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Verwenden Sie das Skript, um eine Schleife durch die aktuelle Wiedergabeliste auszuführen. Verwenden Sie <em>Media</em>. <strong>isIdentical,</strong> um jeden Eintrag in der Wiedergabeliste mit dem <em>Player zu vergleichen.</em> <strong>currentMedia-Objekt.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Verwenden Sie <em>Media</em>. <strong>getMarkerName</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Verwenden Sie <em>Media</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Verwenden Sie <em>Media</em>. <strong>getItemInfo</strong>, <em>Media</em>. <strong>getItemInfoByAtom</strong>und die zugehörigen Methoden zum Abrufen von Metadaten.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Verwenden Sie <em>die Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medienelements. Verwenden Sie dann <em>Media</em>. <strong>getItemInfo</strong> zum Abrufen der Parameterzeichenfolge.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Verwenden Sie <em>die Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medienelements. Verwenden Sie dann <em>Media</em>. <strong>getAttributeName</strong> zum Abrufen der Parameterzeichenfolge.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Wenn derzeit ein Titel wiedergegeben wird, verwenden Sie <em>currentPlaylist.</em> <strong>count</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamGroup</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamSelected</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetSubpictureLanguage</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GoUp</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>zurück.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsSoundCardEnabled</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>LeftButtonSelect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LowerButtonSelect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MenuCall</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>titleMenu</strong> oder <em>DVD</em>. <strong>topMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Weiter</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>weiter.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>weiter.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Öffnen</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>. Dateien werden immer asynchron geöffnet.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Anhalten</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>anhalten.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Wiedergabe</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>wieder.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Zurück</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>zurück.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>zurück.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>fortsetzen.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Rufen Sie ein Medienobjekt mit <em>currentPlaylist ab.</em> <strong>item</strong>(<em>entryNumber</em>). Geben Sie dann das abgerufene Medienobjekt mithilfe von <em>Controls an.</em> <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>wieder.</strong> Alternativ können Sie Controls <em>verwenden.</em> <strong>Als Nächstes,</strong> wenn sich derzeit noch im Modus befindet.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Beenden</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>beenden Sie</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>Nicht verfügbar. Verwenden Sie <em>Steuerelemente.</em> <strong>currentAudioLanguage,</strong> um einen Audiosprachstream anzugeben.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>Verwenden Sie in der Stammwiedergabeliste <em>currentPlaylist</em>. <strong>item</strong>(<em>index</em>) zum Abrufen eines Medienobjekts. Legen Sie dann das Medienobjekt mitHilfe von <em>Controls</em>als aktuelles fest. <strong>currentItem</strong>. Geben Sie dann <em>Controls</em>an. <strong>currentPosition</strong> mit einem Zeitwert in Sekunden.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Verwenden Sie <em>Steuerelemente.</em> <strong>currentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Wenn Sie die angegebene Titelwiedergabeliste bereits wiedergeben, rufen Sie das gewünschte Kapitel mithilfe der folgenden Syntax als Medienobjekt ab:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie dann <em>Player</em>an. <strong>currentMedia</strong> unter Verwendung des zurückgegebenen Medienobjekts.<br/> Alternativ können Sie <em>currentPlaylist</em>verwenden. <strong>Item</strong> zum Abrufen eines Medienobjekts und verwenden dann das zurückgegebene Medienobjekt, um <em>Controls</em>anzugeben. <strong>currentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TopPGSearch</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>UOPValid</strong></td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UpperButtonSelect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Objektmodellereignisse Windows Media Player Version 6.4 mit dem objektmodell Windows Media Player 7 oder höher verglichen.



| Windows Media Player 6.4-Ereignis  | Windows Media Player 7 oder höher                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Pufferung**         | Verwenden Sie *Player*. **Puffern von**.                                                                                                                                                                                              |
| *Player6*. **Klicken Sie auf**             | Verwenden Sie *Player*. **Klicken Sie auf**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Verwenden Sie *Player*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Trennen der Verbindung**        | Nicht verfügbar.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | Nicht verfügbar.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Player*. **DomainChange** und *Player*. **OpenPlaylistSwitch** sind DVD-spezifische Ereignisse. Je nach Anwendung können auch andere Ereignisse im Zusammenhang mit Wiedergabelisten, Medien und CD-ROM-Medien gelten.                        |
| *Player6*. **EndOfStream**       | Verwenden Sie *Player*. **PlayState**.                                                                                                                                                                                              |
| *Player6*. **Fehler**             | Das Ereignis ist unverändert. Fehler werden jedoch in die Warteschlange eingereiht. Verwenden Sie das **Error-Objekt** mit dem **ErrorItem-Objekt,** um Fehlerinformationen aus der Warteschlange abzurufen. Sehen Sie sich den Beispielcode im vorherigen Abschnitt Fehlerbehandlung an. |
| *Player6*. **KeyDown**           | Verwenden Sie *Player*. **Keydown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Verwenden Sie *Player*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Verwenden Sie *Player*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Verwenden Sie *Player*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Verwenden Sie *Player*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Verwenden Sie *Player*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Verwenden Sie *Player*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Verwenden Sie *Player*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Verwenden Sie *Player*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Verwenden Sie *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Verwenden Sie *Player*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Verwenden Sie *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **ScriptCommand**     | Verwenden Sie *Player*. **ScriptCommand**.                                                                                                                                                                                          |
| *Player6*. **Warnung**           | Nicht verfügbar.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zur Migration von Objektmodellen**](object-model-migration-guide.md)
</dt> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





