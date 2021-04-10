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
# <a name="detailed-object-model-comparison"></a>Vergleich von detaillierten Objekt Modellen

In der folgenden Tabelle werden die Eigenschaften des Windows Media Player 6,4-Objektmodells mit dem Objektmodell Windows Media Player 7 oder höher verglichen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6,4-Eigenschaft</th>
<th>Entsprechung für Windows Media Player 7 oder höher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>Allowchangedisplaysize</strong></td>
<td>Die Anzeige von Windows Media Player 7 oder höher wird automatisch an die Medien angepasst. Sie können die Eigenschaften für Höhe und Breite im- <OBJECT> Tag oder im-Skript festlegen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Allowscan</strong></td>
<td>-Steuer <em>Elemente</em>. <strong>FastForward</strong> -und-Steuer <em>Elemente</em>. <strong>fastreverse</strong> sind automatisch für Dateitypen aktiviert, die diese Methoden unterstützen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Anglesavailable</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Animationatstart</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Audiostream</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguageindex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Audiostreamsavailable</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>audiolanguagecount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Autorewind</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong> im Skript, um die aktuelle Position anzugeben oder abzurufen. Verwenden Sie alternativ Marker und den <em>Player</em>. <strong>markerhit</strong> -Ereignis.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AutoSize</strong></td>
<td>Die automatische Größenanpassung ist das Standardverhalten. Wenn Sie die automatische Größenanpassung überschreiben möchten, legen Sie die Eigenschaften Height und Width im- <OBJECT> Tag oder im-Skript fest</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Autostart</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Autostart</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Gleichgewicht</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Bandbreite</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>Bandbreite</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Baseurl</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>baseurl</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Bufferingcount</strong></td>
<td><em>Netzwerk verwenden.</em> <strong>bufferingcount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>BufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>BufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Buttonsavailable</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Canpreview</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Canscan</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong>( &quot; FastForward &quot; ) und Steuer <em>Elemente</em>.<strong> IsAvailable</strong>( &quot; fastreverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong> , um zu testen, ob eine bestimmte Seek-Methode ausgeführt werden kann.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Canseektomarkers</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>IsAvailable</strong>( &quot; currentmarker &quot; ). Verwenden Sie <em>Medien</em>. <strong>markercount</strong> , um die Anzahl von Markern in einem bestimmten Medien Element abzurufen. Verwenden Sie Steuer <em>Elemente</em>. <strong>currentmarker</strong> zum angeben oder Abrufen der aktuellen Markernummer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Captioningid</strong></td>
<td>Verwenden Sie <em>closedcaption</em>. <strong>captioningid</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Ccactive</strong></td>
<td>Nicht verfügbar. Informationen <a href="closed-captioning.md">dazu,</a> wie sich Untertitel in Windows Media Player geändert haben, finden Sie unter Untertitel.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Channeldescription</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Channelurl</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Clicktoplay</strong></td>
<td>Nicht verfügbar. Sie sollten Steuerelemente in der Benutzeroberfläche bereitstellen, um die Wiedergabe zu starten. Alternativ kann der Benutzer mit der rechten Maustaste auf das Videobild klicken, um ein Popup Menü zu öffnen, das eine <strong>Wiedergabe</strong> -/Unterbrechungs Auswahl bei <em>Player</em>enthält. <strong>enablecontextmenu</strong> ist "true".</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Nicht verfügbar. Mit der Windows Media Player 9-Serie oder höher kann der Benutzer auswählen, ob eine eindeutige Player-ID an Inhaltsanbieter übertragen wird.<br/> Wenn der Benutzer diese Option auswählt, sendet der Spieler eine eindeutige ID an den Windows Media-Server. Die ID wird in der Protokolldatei des Servers protokolliert, die sich in der befindet. <em>system32\logfiles unter</em> Ordner standardmäßig. Der Name des Protokoll Felds ist &quot; c-playerid &quot; . Die Server Protokollierung ist in Windows Media Services standardmäßig nicht aktiviert.<br/> Wenn der Benutzer diese Option nicht aktiviert, generiert der Server eine zufällige Sitzungs-ID, die für jeden Client für eine bestimmte Sitzung eindeutig ist.<br/> Weitere Informationen finden Sie in der Dokumentation zu Windows Media Services 9-Serie.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Codeccount</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Colorkey</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Nicht verfügbar. <em>Netzwerk</em>verwenden. <strong>Bitrate</strong> zum Bestimmen der aktuellen Bitrate.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Contactaddress</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Contactphone</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. " <strong>Erdate</strong> "</td>
<td>Verwenden Sie <em>mediacollection</em>. <strong>getmediaatom</strong>(" &quot; &quot; Erstellungsdatum"), um den Index des Erstellungs Datums Atom abzurufen. Verwenden Sie <em>Medien</em>. <strong>getiteminfobyatom</strong> zum Abrufen der Metadaten.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Currentangle</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currentaudiostream</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguageindex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Currentbutton</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currentccservice</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Rufen Sie die aktuelle Wiedergabeliste ab. , Wenn die aktuelle Wiedergabeliste nicht die gleiche ist wie die von <em>CDROM</em>zurückgegebene Wiedergabeliste. <strong>Wiedergabeliste</strong>, dann gibt es kein Aktuelles Kapitel. Andernfalls ist die aktuelle Kapitel Nummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currentdiscside</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>Domäne</strong>:</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currentmarker</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentmarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currentsubpicturestream</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentPositionTimecode</strong>, Steuer <em>Elemente</em>. <strong>currentpositionstring</strong>, oder-Steuer <em>Elemente</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Currenttitle</strong></td>
<td>Rufen Sie die aktuelle Wiedergabeliste ab. , Wenn die aktuelle Wiedergabeliste dieselbe wie die von <em>CDROM</em>zurückgegebene Wiedergabeliste ist. <strong>Wiedergabeliste</strong>, dann ist die Titel Nummer der Index des aktuellen Mediums in der aktuellen Wiedergabeliste.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Currentvolume</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Cursor Type</strong></td>
<td>Nicht verfügbar. Verwenden Sie stattdessen Internet Explorer-Stile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Defaultframe</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>defaultframe</strong>oder Verwenden eines <PARAM> -Attribut im- <OBJECT> Element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Display BackColor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Display ForeColor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>Die aktuelle Position kann in Sekunden von Anfang an als <strong>Zahl</strong> mithilfe von-Steuer <em>Elementen</em>abgerufen werden. <strong>CurrentPosition</strong>als <strong>Zeichen</strong> Folge, die als hh: mm: SS (Stunden, Minuten, Sekunden) mit Steuer <em>Elementen</em>formatiert ist. <strong>currentpositionstring</strong>oder im Zeit Code Format mithilfe von-Steuer <em>Elementen</em>. <strong>currentPositionTimecode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Display</strong></td>
<td>Die Standard Anzeige wird automatisch an die Medien angepasst. Sie können die Eigenschaften für Höhe und Breite im- <OBJECT> Tag oder im Skript festlegen. Verwenden Sie <em>Player</em>. <strong>Vollbild</strong> , um in den Vollbildmodus zu wechseln.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Dauer</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>Dauer</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>DVD</strong>:</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Enablecontextmenu</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>enablecontextmenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Aktiviert</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>aktiviert</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Enablefullscreencontrols</strong></td>
<td>Wenn Sie Windows Media Player 9 oder höher verwenden, werden voll Bild Steuerelemente automatisch aktiviert, es sei denn, <em>Player</em>. <strong>uiMode</strong>  =  &quot; keine &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Enablepositioncontrols</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Enabletracker</strong></td>
<td>Nicht verfügbar. Sie können ein benutzerdefiniertes Steuerelement bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Entrycount</strong></td>
<td>Verwenden Sie <em>Wiedergabeliste</em>. <strong>Anzahl</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Verwenden Sie <em>ErrorItem</em>. <strong>errorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Errorkorrektur</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Verwenden Sie <em>ErrorItem</em>. <strong>ErrorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Dateiname</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>. Verwenden Sie Steuer <em>Elemente</em>. ein Ereignis, <strong>das beim Arbeiten</strong> innerhalb einer Wiedergabeliste angezeigt wird.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td><em>Fehler</em>bei Verwendung. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Hasmultipleitems</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Imagesourceheight</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>imagesourceheight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Imagesourcewidth</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>imagesourcewidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Invokeurls</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>invokeurls</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Isbroadcast</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>sourceprotocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Isdurationvalid</strong></td>
<td>Nicht verfügbar. <em>Medien</em>: die <strong>Dauer</strong> enthält einen gültigen Wert, wenn Sie mit dem aktuellen Medienobjekt verwendet wird.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sprache</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Lostpakete</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>lostpakete</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Markercount</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>markercount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Stumm schalten</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>stumm schalten</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Openstate</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>openstate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Playcount</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>playcount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Playstate</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>playstate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Nicht verfügbar. Verwenden Sie eine Skript Schleifen Struktur mit einem HTML-Timer, um diese Funktionalität zu duplizieren.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Rate</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. Read- <strong>State</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>openstate</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Receivedpakete</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>receivedpakete</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. " <strong>Receptionquality</strong> "</td>
<td><em>Netzwerk</em>verwenden. " <strong>receptionquality</strong>".</td>
</tr>
<tr class="even">
<td><em>Player6</em>. Wieder <strong>herstellbare Pakete</strong></td>
<td><em>Netzwerk</em>verwenden. wieder <strong>herstellbare Pakete</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong></strong> Stamm</td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Samifilename</strong></td>
<td>Verwenden Sie <em>closedcaption</em>. <strong>Samifilename</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Samilang</strong></td>
<td>Verwenden Sie <em>closedcaption</em>. <strong>Samilang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Samistyle</strong></td>
<td>Verwenden Sie <em>closedcaption</em>. <strong>Samistyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>Dauer</strong> zur Bestimmung der Länge eines <strong>Medien</strong> Objekts. Verwenden Sie einen Marker mit-Steuer <em>Elementen</em>. <strong>currentmarker</strong> , um eine benutzerdefinierte Endposition anzugeben.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong> , um die Wiedergabe an einer bestimmten Position zu starten oder einen Marker mit Steuer <em>Elementen</em>zu verwenden. <strong>currentmarker</strong> zum Angeben einer benutzerdefinierten Startposition.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Senderrorevents</strong></td>
<td>Fehler werden in die Warteschlange gestellt. Verwenden Sie das <strong>Error</strong> -Objekt und das <strong>ErrorItem</strong> -Objekt, um Fehlerinformationen abzurufen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sendkeyboarentvents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Sendmouserclickevents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sendmousermuveevents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Sendopenstatechangeevents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sendplaystatechangeevents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Sendwarningevents</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Showaudiocontrols</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Show</strong> Titel</td>
<td>Nicht verfügbar. Sie können eine benutzerdefinierte geschlossene Beschriftungs Anzeige angeben.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Show Display</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Showgoinfo-Leiste</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Funktionen mit dem Medienobjekt bereitstellen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Showpositioncontrols</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Showtracker</strong></td>
<td>Nicht verfügbar. Sie können benutzerdefinierte Steuerelemente bereitstellen oder <em>Player</em>verwenden. <strong>uiMode</strong> , um eine Standardkonfiguration auszuwählen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sourcelink</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>SourceUrl</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Sourceprotocol</strong></td>
<td><em>Netzwerk</em>verwenden. <strong>sourceprotocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Nicht verfügbar. Verwenden Sie Steuer <em>Elemente</em>. <strong>audiolanguagecount</strong> zum Abrufen der Anzahl der audiosprachstreams.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Subpictureon</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Subpicturestreamsavailable</strong></td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Titlesavailable</strong></td>
<td>Verwenden Sie Folgendes:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Totaltitletime</strong></td>
<td>Verwenden Sie <em>currentMedia</em>. <strong>Dauer</strong> oder <em>currentMedia</em>. <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Transparentatstart</strong></td>
<td>Verwenden Sie Skripts, um die Höhen-und Breitenwerte anzugeben, um den Player sichtbar oder unsichtbar zu machen.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueId</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Videobordercolor</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Videoborderwidth</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volume</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Volume</strong>:</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Volumesesverfügbar</strong></td>
<td>Nicht verfügbar.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Objektmodell Methoden von Windows Media Player, Version 6,4, mit dem Objektmodell Windows Media Player 7 oder höher verglichen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6,4-Methode</th>
<th>Entsprechung für Windows Media Player 7 oder höher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>Abgangsbox</strong></td>
<td>Verwenden Sie <em>Player</em>. <strong>VERSIONINFO</strong> zum Abrufen der Windows-Version Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Backwardscan</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Buttonaktivierung</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Buttonselectandaktivierungs</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abbrechen</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. " <strong>Chapterplay</strong> "</td>
<td>Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. " <strong>Chapterplayautostoppt</strong> "</td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. " <strong>Chaptersearch</strong> "</td>
<td>Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>FastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Fastreverse</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>fastreverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Forwardscan</strong></td>
<td>Verwenden Sie <em>Einstellungen</em>. <strong>Rate</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getallgprms</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getallsprms</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getaudiolanguage</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong> zum Abrufen der LCID der aktuellen Audiosprache.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getcodecdescription</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getcodecinstallation</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getcodecurl</strong></td>
<td>Verwenden Sie <em>ErrorItem</em>. <strong>CustomURL</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getcurrententry</strong></td>
<td>Verwenden Sie das Skript zum Durchlaufen der aktuellen Wiedergabeliste. Verwenden Sie <em>Medien</em>. <strong>isidentical</strong> zum Vergleichen der einzelnen Einträge in der Wiedergabeliste mit dem <em>Player</em>. <strong>currentMedia</strong> -Objekt.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getmarkername</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>getmarkername</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getmarkertime</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>getmarkertime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getmediainfostring</strong></td>
<td>Verwenden Sie <em>Medien</em>. <strong>getiteminfo</strong>, <em>Medium</em>. <strong>getiteminfobyatom</strong>und die zugehörigen Methoden zum Abrufen von Metadaten.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getmediaparameter</strong></td>
<td>Verwenden Sie <em>Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medien Elements. Verwenden Sie dann die- <em>Medien</em>. <strong>getiteminfo</strong> zum Abrufen der Parameter Zeichenfolge.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getmediaparametername</strong></td>
<td>Verwenden Sie <em>Wiedergabeliste</em>. <strong>Element</strong> zum Abrufen eines Medien Elements. Verwenden Sie dann die- <em>Medien</em>. <strong>GetAttributeName</strong> zum Abrufen der Parameter Zeichenfolge.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getmoreingefourl</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getnumofchapters</strong></td>
<td>Wenn gerade ein Titel wiedergegeben wird, verwenden Sie <em>currentwiedergabe</em>. <strong>Anzahl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getstreamgroup</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getstreamselected</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getsubpicturelanguage</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Goup</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>zurück</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Issoundcardenabled</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Leftbuttonselect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Lowerbuttonselect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Menucall</strong></td>
<td>Verwenden Sie <em>DVD</em>. <strong>titlemenu</strong> oder <em>DVD</em>. <strong>topmenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Nächste</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>als nächstes</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Nextpgsearch</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>als nächstes</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Öffnen</strong> Sie</td>
<td>Verwenden Sie <em>Player</em>. <strong>URL</strong> oder <em>Player</em>. <strong>currentMedia</strong>. Dateien werden immer asynchron geöffnet.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong></strong> Anhalten</td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong></strong>anhalten.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong></strong> Wiedergeben</td>
<td>Verwenden Sie Steuer <em>Elemente</em>. wieder <strong>geben.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Vorheriges</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>Vorheriges</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Prevpgsearch</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>Vorheriges</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Resumefrommenu</strong></td>
<td>Verwenden Sie <em>DVD</em>. fort <strong>setzen.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Rightbuttonselect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Setcurrententry</strong></td>
<td>Rufen Sie mithilfe von <em>currentwiedergabe</em>ein Medienobjekt ab. <strong>Item</strong>(<em>entrynumber</em>). Geben Sie dann das abgerufene Medienobjekt mithilfe von Steuer <em>Elementen</em>an. der- <strong>Typ.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Show Dialog</strong></td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Stilloff</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. wieder <strong>geben.</strong> Verwenden Sie alternativ Steuer <em>Elemente</em>. <strong>Als nächstes</strong> , wenn sich derzeit im immer noch Modus befindet.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. Wird <strong>beendet</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>beendet</strong>wird.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Streamselect</strong></td>
<td>Nicht verfügbar. Verwenden Sie Steuer <em>Elemente</em>. <strong>currentaudiolanguage</strong> zur Angabe eines audiosprachstreams.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Timeplay</strong></td>
<td>Verwenden Sie in der Stamm Wiedergabeliste <em>currentwiedergabe</em>. <strong>Element</strong>(<em>Index</em>) zum Abrufen eines Medien Objekts. Legen Sie dann das Medienobjekt mithilfe von-Steuer <em>Elementen</em>als Aktuelles fest. der- <strong>Typ.</strong> Geben Sie dann Steuer <em>Elemente</em>an. <strong>CurrentPosition</strong> mit einem Uhrzeitwert in Sekunden.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Timesearch</strong></td>
<td>Verwenden Sie Steuer <em>Elemente</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Titleplay</strong></td>
<td>Wenn die angegebene Titel Wiedergabeliste bereits verwendet wird, rufen Sie das gewünschte Kapitel als Medienobjekt ab, indem Sie die folgende Syntax verwenden:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Geben Sie anschließend <em>Player</em>an. <strong>currentMedia</strong> mit dem zurückgegebenen Medienobjekt.<br/> Verwenden Sie alternativ <em>currentwiedergabe</em>. <strong>Element</strong> zum Abrufen eines Medien Objekts, und verwenden Sie dann das zurückgegebene Medienobjekt, um Steuer <em>Elemente</em>anzugeben. der- <strong>Typ.</strong><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. " <strong>Toppgsearch</strong> "</td>
<td>Nicht verfügbar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Uopvalid</strong></td>
<td>Nicht verfügbar</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Upperbuttonselect</strong></td>
<td>Nicht verfügbar.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle werden die Objektmodell Ereignisse von Windows Media Player, Version 6,4, mit dem Objektmodell Windows Media Player 7 oder höher verglichen.



| Windows Media Player 6,4-Ereignis  | Entsprechung für Windows Media Player 7 oder höher                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Pufferung**         | Verwenden Sie *Player*. **Pufferung**.                                                                                                                                                                                              |
| *Player6*. **Klicken Sie auf**             | Verwenden Sie *Player*. **Klicken Sie auf**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Verwenden Sie *Player*. **Doppelklick**                                                                                                                                                                                             |
| *Player6*. Verbindung **trennen**        | Nicht verfügbar.                                                                                                                                                                                                           |
| *Player6*. **Displaymodechange** | Nicht verfügbar.                                                                                                                                                                                                           |
| *Player6*. **Dvdnotify**         | *Player*. **Domainchange** und *Player*. **Openplaylistswitch** sind DVD-spezifische Ereignisse. Abhängig von der Anwendung können auch andere Ereignisse in Zusammenhang mit Wiedergabe-, Medien-und CD-ROM-Medien angewendet werden.                        |
| *Player6*. **EndOf-Stream**       | Verwenden Sie *Player*. **Playstate**.                                                                                                                                                                                              |
| *Player6*. **Fehler**             | Das Ereignis ist unverändert. Fehler werden jedoch in die Warteschlange eingereiht. Verwenden Sie das **Error** -Objekt mit dem **ErrorItem** -Objekt, um Fehlerinformationen aus der Warteschlange abzurufen. Sehen Sie sich den Beispielcode im vorherigen Abschnitt Fehlerbehandlung an. |
| *Player6*. **KeyDown**           | Verwenden Sie *Player*. **KeyDown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Verwenden Sie *Player*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Verwenden Sie *Player*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **Markerhit**         | Verwenden Sie *Player*. **Markerhit**.                                                                                                                                                                                              |
| *Player6*. **Mouum**         | Verwenden Sie *Player*. **Mouum**                                                                                                                                                                                               |
| *Player6*. **Mouseelmove**         | Verwenden Sie *Player*. **Mouseelmove**                                                                                                                                                                                               |
| *Player6*. **Mouberup**           | Verwenden Sie *Player*. **Mouberup**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Verwenden Sie *Player*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Verwenden Sie *Player*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Verwenden Sie *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **Positionsänderung**    | Verwenden Sie *Player*. **Positionsänderung**.                                                                                                                                                                                         |
| *Player6*. " **Leserystatechange** "  | Verwenden Sie *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **ScriptCommand**     | Verwenden Sie *Player*. **ScriptCommand**.                                                                                                                                                                                          |
| *Player6*. **Warnung**           | Nicht verfügbar.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





