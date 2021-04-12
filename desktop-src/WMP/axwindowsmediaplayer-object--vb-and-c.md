---
title: AxWindowsMediaPlayer-Objekt (VB and C )
description: AxWindowsMediaPlayer-Objekt (VB und C \)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Windows Media Player, AxWindowsMediaPlayer-Objekt
- Windows Media Player Mobile, AxWindowsMediaPlayer-Objekt
- Windows Media Player-Objektmodell, AxWindowsMediaPlayer-Objekt
- Objektmodell, AxWindowsMediaPlayer-Objekt
- ActiveX-Steuerelement, AxWindowsMediaPlayer-Objekt
- Windows Media Player ActiveX-Steuerelement, AxWindowsMediaPlayer-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, AxWindowsMediaPlayer-Objekt
- Verweis für Objektmodell, AxWindowsMediaPlayer-Objekt
- AxWindowsMediaPlayer-Objekt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f814560c8b6eb13dc5abb8736378432ec4565e
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104472420"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>AxWindowsMediaPlayer-Objekt (VB und c#)

Das AxWindowsMediaPlayer-Objekt ist das Stamm Objekt für das Windows Media Player-Steuerelement. Die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgelistet sind, werden unterstützt.

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                                                             | BESCHREIBUNG                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromcollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Ruft eine **iwmpcdromcollection** -Schnittstelle ab.                                                                                         |
| [closedcaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Ruft eine iwmpclosedcaption-Schnittstelle ab.                                                                                               |
| [CTL-Steuerelemente](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Ruft eine iwmpcontrols-Schnittstelle ab.                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement aktiviert ist                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Ruft die iwmpmedia-Schnittstelle ab, die dem aktuellen Medien Element entspricht, oder legt diese fest.                                                   |
| [currentwiedergabe](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Ruft die aktuelle **iwmpwiedergabe** -Schnittstelle ab oder legt Sie fest.                                                                               |
| [DVD](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Ruft eine iwmpdvd-Schnittstelle ab.                                                                                                         |
| [enablecontextmenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder legt diesen fest.          |
| [Fehler](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Ruft eine iwmperror-Schnittstelle ab.                                                                                                       |
| [Vollbild](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Ruft einen Wert ab, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder legt diesen fest.                                          |
| [IsOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Ruft einen Wert ab, der angibt, ob der Benutzer mit einem Netzwerk verbunden ist.                                                                |
| IsRemote                                                                             | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                |
| [mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Ruft eine iwmpmediacollection-Schnittstelle ab.                                                                                             |
| [network](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Ruft eine iwmpnetwork-Schnittstelle ab.                                                                                                     |
| [openstate](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.                                                                           |
| playerapplication                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                |
| [playlistcollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Ruft eine iwmpplaylistcollection-Schnittstelle ab.                                                                                          |
| [playstate](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.                                                           |
| [settings](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Ruft eine iwmpsettings-Schnittstelle ab.                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Ruft einen Wert ab, der den aktuellen Status von Windows-Media Player angibt.                                                                |
| [stretchdefit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Video auf die Größe der Windows-Media Player Steuerelement-Videoanzeige gestreckt wird          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Ruft einen Wert ab, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden, wenn Windows Media Player in eine Webseite eingebettet ist, oder legt diesen fest. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Ruft den Namen des wieder zugebende Clips ab oder legt diesen fest.                                                                                         |
| [VERSIONINFO](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Ruft einen-Wert ab, der die Version des Windows-Media Player angibt.                                                               |
| [windowlessvideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert, oder legt diesen fest                         |



 

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Methoden.



| Methode                                                       | BESCHREIBUNG                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Gibt Windows Media Player-Ressourcen frei.                  |
| [launchurl](axwmplib-axwindowsmediaplayer-launchurl.md)     | Sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. |
| [newmedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Gibt eine iwmpmedia-Schnittstelle für ein neues Medien Element zurück.      |
| [neue](axwmplib-axwindowsmediaplayer-newplaylist.md) | gibt eine iwmpwiedergabe-Schnittstelle für eine neue Wiedergabeliste zurück.     |
| [openplayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | Öffnet Windows-Media Player mit der angegebenen URL.       |



 

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Ereignisse.



| Ereignis                                                                                                              | BESCHREIBUNG                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Audiolanguagechange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Tritt auf, wenn sich die aktuelle Audiosprache ändert.                                                            |
| [Pufferung](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung startet oder beendet.                                     |
| [Cdromburnerror](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Tritt auf, wenn während eines CD-Brennvorgangs ein generischer Fehler auftritt.                                         |
| [Cdromburnmediaerror](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Tritt auf, wenn beim Brennen eines einzelnen Medien Elements auf einer CD ein Fehler auftritt.                               |
| [Cdromburnstatechange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Tritt auf, wenn der Zustand eines CD-Brennvorgangs geändert wird.                                                          |
| [Cdrommediachange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Tritt auf, wenn eine CD oder DVD in ein CD-oder DVD-Laufwerk eingefügt oder von dort aus entfernt wird.                                |
| [Cdromripmediaerror](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Tritt auf, wenn ein Fehler auftritt, während ein einzelner Track von einer CD gerippt wird.                                  |
| [Cdromripstatechange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Tritt auf, wenn sich ein CD-einreißen-Vorgang ändert.                                                          |
| [Klicken](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Tritt ein, wenn der Benutzer auf eine Maustaste klickt.                                                                |
| "Kreatepartnershipcomplete"                                                                                          | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Ereignis Wechsel](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Tritt auf, wenn [iwmpcontrols.](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) Currency Item geändert wird. |
| [Currentmediaitemavailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird.                           |
| [Currentplaylistchange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.                                                 |
| [Currentplaylistitemavailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Tritt ein, wenn das aktuelle Wiedergabelisten Element verfügbar wird.                                                   |
| DeviceConnect                                                                                                      | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Devicedisconnect                                                                                                   | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Devicestatuschange                                                                                                 | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Geräte Fehlercode                                                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Devicesyncstatechange                                                                                              | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Disconnect](axwmplib-axwindowsmediaplayer-disconnect.md) (Trennen)                                                         | Für die zukünftige Verwendung reserviert.                                                                                   |
| [Domainchange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Tritt auf, wenn die DVD-Domäne geändert wird.                                                                        |
| [DoubleClick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Tritt ein, wenn der Benutzer auf eine Maustaste doppelklickt.                                                         |
| [Durationunitchange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Für die zukünftige Verwendung reserviert.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Für die zukünftige Verwendung reserviert.                                                                                   |
| [Fehler](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.                                       |
| [Folderscanstatechange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Tritt auf, wenn der Status einer Ordner Überwachung geändert wird.                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Tritt beim Drücken einer Taste ein.                                                                              |
| [KeyPress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Tritt auf, wenn eine Taste gedrückt und anschließend freigegeben wird.                                                            |
| [KeyUp](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Tritt ein, wenn eine Taste losgelassen wird.                                                                             |
| [Libraryconnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Tritt auf, wenn eine Bibliothek verfügbar wird.                                                                   |
| [Librarydisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.                                                              |
| [Markerhit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Tritt ein, wenn ein Marker erreicht wird.                                                                           |
| [Mediachange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Tritt auf, wenn ein Medien Element geändert wird.                                                                          |
| [Mediacollectionattributestringadded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.                                                    |
| [Mediacollectionattributestringchanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.                                                  |
| [Mediacollectionattributestraningrebewegt](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.                                                |
| [Mediacollectionchange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Tritt auf, wenn die Mediensammlung geändert wird.                                                                  |
| [Mediacollectionmediaadded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Tritt auf, wenn der lokalen Bibliothek ein Medien Element hinzugefügt wird.                                                    |
| [Mediacollectionmediarebewegt](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.                                                   |
| [Modeänderung](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Tritt auf, wenn ein Windows Media Player-Modus geändert wird.                                                     |
| [MouseDown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Tritt auf, wenn eine Maustaste gedrückt wird.                                                                     |
| [MouseMove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Tritt ein, wenn der Mauszeiger verschoben wird.                                                                    |
| [MouseUp](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Tritt auf, wenn eine Maustaste losgelassen wird.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Für die zukünftige Verwendung reserviert.                                                                                   |
| [Openplaylistswitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Tritt auf, wenn sich der Zustand des Windows Media Player-Steuer Elements ändert                                                |
| Playerdockedstatechange                                                                                            | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Playerreconnect                                                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Playlistchange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Tritt auf, wenn eine Wiedergabeliste geändert wird.                                                                            |
| [Playlistcollectionchange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Tritt auf, wenn sich etwas in der Wiedergabelisten Auflistung ändert.                                                  |
| [Playlistcollectionplaylistadded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.                                                |
| [Playlistcollectionplaylistreverschohe](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.                                            |
| [Playlistcollectionplaylisteintasdeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Für die zukünftige Verwendung reserviert.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Tritt auf, wenn sich der Wiedergabe Zustand des Windows-Media Player Steuer Elements ändert.                                    |
| [Positionsänderung](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Tritt ein, wenn die aktuelle Position des Medien Elements geändert wurde.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Tritt auf, wenn ein synchronisierter Befehl oder eine URL empfangen wird.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Tritt ein, wenn der Wert der **Status** Eigenschaft geändert wird.                                                         |
| [Stringcollectionchange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Tritt auf, wenn eine Zeichen folgen Auflistung geändert wird.                                                                   |
| Switchedto Control                                                                                                  | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| Switchedtoplayerapplication                                                                                        | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Warnung](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Für die zukünftige Verwendung reserviert.                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Iwmperror-Schnittstelle (VB und c#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Objektmodell Referenz für Visual Basic .net und C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Wmpopenstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




