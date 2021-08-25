---
title: AxWindowsMediaPlayer-Objekt (VB and C )
description: AxWindowsMediaPlayer-Objekt (VB und C\)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Windows Media Player,AxWindowsMediaPlayer-Objekt
- Windows Media Player Mobile,AxWindowsMediaPlayer-Objekt
- Windows Media Player Objektmodell,AxWindowsMediaPlayer-Objekt
- Objektmodell,AxWindowsMediaPlayer-Objekt
- ActiveX-Steuerelement, AxWindowsMediaPlayer-Objekt
- Windows Media Player ActiveX-Steuerelement, AxWindowsMediaPlayer-Objekt
- Windows Media Player Mobiles ActiveX-Steuerelement,AxWindowsMediaPlayer-Objekt
- Referenz für Objektmodell,AxWindowsMediaPlayer-Objekt
- AxWindowsMediaPlayer-Objekt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d0c66360e80ea293795442472ce163292c38152baa859889086a5687f03764f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765280"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>AxWindowsMediaPlayer-Objekt (VB und C#)

Das AxWindowsMediaPlayer-Objekt ist das Stammobjekt für das Windows Media Player-Steuerelement. Sie unterstützt die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgeführt sind.

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                                                             | Beschreibung                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [ccollectionCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Ruft eine **IWMPCcollectionCollection-Schnittstelle** ab.                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Ruft eine IWMPClosedCaption-Schnittstelle ab.                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Ruft eine IWMPControls-Schnittstelle ab.                                                                                                    |
| [Strgbard](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement aktiviert ist, oder legt einen Wert fest.                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Ruft die IWMPMedia-Schnittstelle ab, die dem aktuellen Medienelement entspricht, oder legt sie fest.                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Ruft die aktuelle **IWMPPlaylist-Schnittstelle** ab oder legt sie fest.                                                                               |
| [Dvd](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Ruft eine IWMPDVD-Schnittstelle ab.                                                                                                         |
| [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird, oder legt diesen fest.          |
| [Fehler](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Ruft eine IWMPError-Schnittstelle ab.                                                                                                       |
| [Fullscreen](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Ruft einen Wert ab, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder legt den Wert fest.                                          |
| [isOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Ruft einen Wert ab, der angibt, ob der Benutzer mit einem Netzwerk verbunden ist.                                                                |
| isRemote                                                                             | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                |
| [mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Ruft eine IWMPMediaCollection-Schnittstelle ab.                                                                                             |
| [network](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Ruft eine IWMPNetwork-Schnittstelle ab.                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.                                                                           |
| playerApplication                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                |
| [playlistCollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Ruft eine IWMPPlaylistCollection-Schnittstelle ab.                                                                                          |
| [playState](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Ruft einen Wert ab, der den Zustand des Windows Media Player Vorgangs angibt.                                                           |
| [settings](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Ruft eine IWMPSettings-Schnittstelle ab.                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Ruft einen Wert ab, der den aktuellen Status von Windows Media Player angibt.                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Ruft einen Wert ab, der angibt, ob das Video an die Größe der Windows Media Player Videoanzeige des Steuerelements angepasst wird, oder legt diesen fest.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Ruft einen Wert ab, der angibt, welche Steuerelemente auf der Benutzeroberfläche angezeigt werden, wenn Windows Media Player in eine Webseite eingebettet ist, oder legt den Wert fest. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Ruft den Namen des abgespielten Clips ab oder legt diesen fest.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Ruft einen Wert ab, der die Version der Windows Media Player angibt.                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement Video im fensterlosen Modus rendert, oder legt den Wert fest.                         |



 

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Methoden.



| Methode                                                       | Beschreibung                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Gibt Windows Media Player Ressourcen frei.                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | Sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. |
| [Newmedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Gibt eine IWMPMedia-Schnittstelle für ein neues Medienelement zurück.      |
| [newPlaylist](axwmplib-axwindowsmediaplayer-newplaylist.md) | gibt eine IWMPPlaylist-Schnittstelle für eine neue Wiedergabeliste zurück.     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | Öffnet Windows Media Player unter Verwendung der angegebenen URL.       |



 

Das AxWindowsMediaPlayer-Objekt unterstützt die folgenden Ereignisse.



| Ereignis                                                                                                              | Beschreibung                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Tritt ein, wenn sich die aktuelle Audiosprache ändert.                                                            |
| [Pufferung](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Tritt ein, wenn das Windows Media Player-Steuerelement mit der Pufferung beginnt oder beendet.                                     |
| [CholeError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Tritt auf, wenn während eines CD-Vorgangs ein generischer Fehler auftritt.                                         |
| [CholeHoleMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Tritt auf, wenn ein Fehler auftritt, während ein einzelnes Medienelement an eine CD ausgegeben wird.                               |
| [CholeStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Tritt ein, wenn sich der Zustand eines CD-Vorgangs ändert.                                                          |
| [CholeMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Tritt ein, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird.                                |
| [CorporaRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Tritt auf, wenn ein Fehler auftritt, während eine einzelne Spur von einer CD entfernt wird.                                  |
| [CorporaRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Tritt ein, wenn sich der Zustand eines CD-Löschvorgangs ändert.                                                          |
| [Klicken](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Tritt ein, wenn der Benutzer auf eine Maustaste klickt.                                                                |
| CreatePartnershipComplete                                                                                          | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Tritt auf, [wenn sich IWMPControls.currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) ändert. |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Tritt ein, wenn ein grafisches Metadatenelement im aktuellen Medienelement verfügbar wird.                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Tritt ein, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Tritt ein, wenn das aktuelle Wiedergabelistenelement verfügbar wird.                                                   |
| DeviceConnect                                                                                                      | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| DeviceDisconnect                                                                                                   | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| DeviceStatusChange                                                                                                 | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| DeviceSyncError                                                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| DeviceSyncStateChange                                                                                              | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Trennen](axwmplib-axwindowsmediaplayer-disconnect.md)                                                          | Für die zukünftige Verwendung reserviert.                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Tritt ein, wenn sich die DVD-Domäne ändert.                                                                        |
| [Doubleclick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Tritt ein, wenn der Benutzer auf eine Maustaste doppelklickt.                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Für die zukünftige Verwendung reserviert.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Für die zukünftige Verwendung reserviert.                                                                                   |
| [Fehler](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Tritt ein, wenn das Windows Media Player-Steuerelement eine Fehlerbedingung auf hat.                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Tritt ein, wenn ein Ordnerüberwachungsvorgang den Zustand ändert.                                                   |
| [Keydown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Tritt beim Drücken einer Taste ein.                                                                              |
| [Keypress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Tritt ein, wenn eine Taste gedrückt und dann freigegeben wird.                                                            |
| [Keyup](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Tritt ein, wenn eine Taste losgelassen wird.                                                                             |
| [LibraryConnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Tritt ein, wenn eine Bibliothek verfügbar wird.                                                                   |
| [LibraryDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Tritt ein, wenn ein Marker erreicht wird.                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Tritt ein, wenn sich ein Medienelement ändert.                                                                          |
| [MediaCollectionAttributeStringAdded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Tritt ein, wenn der Bibliothek ein Attributwert hinzugefügt wird.                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Tritt ein, wenn ein Attributwert in der Bibliothek geändert wird.                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Tritt ein, wenn ein Attributwert aus der Bibliothek entfernt wird.                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Tritt ein, wenn sich die Mediensammlung ändert.                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Tritt ein, wenn der lokalen Bibliothek ein Medienelement hinzugefügt wird.                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Tritt ein, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Tritt auf, wenn das **Media-Objekt** eine Fehlerbedingung auf hat.                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Tritt ein, wenn ein Modus Windows Media Player geändert wird.                                                     |
| [Mousedown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Tritt ein, wenn eine Maustaste gedrückt wird.                                                                     |
| [Mousemove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Tritt ein, wenn der Mauszeiger bewegt wird.                                                                    |
| [Mouseup](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Tritt ein, wenn eine Maustaste losgelassen wird.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Für die zukünftige Verwendung reserviert.                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Tritt ein, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Tritt ein, wenn das Windows Media Player-Steuerelement den Zustand ändert.                                                |
| PlayerDockedStateChange                                                                                            | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| PlayerReconnect                                                                                                    | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Tritt ein, wenn sich eine Wiedergabeliste ändert.                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Tritt ein, wenn sich etwas in der Wiedergabelistensammlung ändert.                                                  |
| [PlaylistCollectionPlaylistAdded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Tritt ein, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird.                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Tritt ein, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird.                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Für die zukünftige Verwendung reserviert.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Tritt ein, wenn sich der Wiedergabezustand des Windows Media Player ändert.                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Tritt ein, wenn die aktuelle Position des Medienelements geändert wurde.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Tritt ein, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Tritt ein, wenn **die Statuseigenschaft** den Wert ändert.                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Tritt ein, wenn sich eine Zeichenfolgenauflistung ändert.                                                                   |
| SwitchedToControl                                                                                                  | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| SwitchedToPlayerApplication                                                                                        | Wird für die .NET-Programmierung nicht unterstützt.                                                                        |
| [Warnung](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Für die zukünftige Verwendung reserviert.                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPCcollectionCollection-Schnittstelle (VB und C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPError-Schnittstelle (VB und C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Objektmodellreferenz für Visual Basic .NET und C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




