---
title: Player-Objekt
description: Das Player-Objekt ist das Stammobjekt für das Windows Media Player-Steuerelement. Sie unterstützt die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgeführt sind.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Player-Objekt Windows Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ee314862aad1237036d5a7fa6a5627f42a6185d1ab6914f1e11ec19a831b755
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616700"
---
# <a name="player-object"></a>Player-Objekt

Das Player-Objekt ist das Stammobjekt für das Windows Media Player-Steuerelement. Sie unterstützt die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgeführt sind.

Das Player-Objekt unterstützt die folgenden Eigenschaften. Eigenschaften, die mit einem Sternchen () gekennzeichnet \* sind, sind für Skins nicht zugänglich.



| Eigenschaft                                             | Beschreibung                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [ccollectionCollection](player-cdromcollection.md)        | Ruft das [CcollectionCollection-Objekt](cdromcollection-object.md) ab.                                                                          |
| [closedCaption](player-closedcaption.md)            | Ruft das [ClosedCaption-Objekt](closedcaption-object.md) ab.                                                                              |
| [Steuerelemente](player-controls.md)                      | Ruft das [Controls-Objekt](controls-object.md) ab.                                                                                        |
| [currentMedia](player-currentmedia.md)              | Gibt das aktuelle [Medienobjekt](media-object.md) an oder ruft es ab.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Gibt das aktuelle [Wiedergabelistenobjekt](playlist-object.md) an oder ruft es ab.                                                                   |
| [Dvd](player-dvd.md)                                | Ruft das [DVD-Objekt](dvd-object.md) ab.                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Gibt einen Wert an, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird, oder ruft diesen ab.          |
| [aktiviert](player-enabled.md)\*                     | Gibt einen Wert an, der angibt, ob das Windows Media Player-Steuerelement aktiviert ist, oder ruft einen Wert ab.                                               |
| [error](player-error.md)                            | Ruft das [Error-Objekt](error-object.md) ab.                                                                                              |
| [fullScreen](player-fullscreen.md)\*               | Gibt einen Wert an, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder ruft einen Wert ab.                                          |
| [isOnline](player-isonline.md)                      | Ruft einen Wert ab, der angibt, ob der Benutzer mit einem Netzwerk verbunden ist.                                                                     |
| [isRemote](player-isremote.md)\*                   | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement im Remotemodus ausgeführt wird.                                             |
| [mediaCollection](player-mediacollection.md)        | Ruft das [MediaCollection-Objekt](mediacollection-object.md) ab.                                                                          |
| [network](player-network.md)                        | Ruft das [Network-Objekt](network-object.md) ab.                                                                                          |
| [openState](player-openstate.md)                    | Ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Ruft das [PlayerApplication-Objekt](playerapplication-object.md) ab, wenn ein Remotesteuerelement Windows Media Player ausgeführt wird.               |
| [playlistCollection](player-playlistcollection.md)  | Ruft das [PlaylistCollection-Objekt](playlistcollection-object.md) ab.                                                                    |
| [playState](player-playstate.md)                    | Ruft einen Wert ab, der den Status des Windows Media Player Vorgangs angibt.                                                                |
| [settings](player-settings.md)                      | Ruft das [Einstellungen-Objekt](settings-object.md) ab.                                                                                        |
| [status](player-status.md)                          | Ruft einen Wert ab, der den aktuellen Status von Windows Media Player angibt.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Gibt einen Wert an, der angibt, ob das Video an die Größe des Windows Media Player Videoanzeige angepasst wird, oder ruft diesen ab.          |
| [uiMode](player-uimode.md)\*                       | Gibt einen Wert an, der angibt, welche Steuerelemente auf der Benutzeroberfläche angezeigt werden, wenn Windows Media Player in eine Webseite eingebettet ist, oder ruft einen Wert ab. |
| [URL](player-url.md)                                | Gibt den Namen des abgespielten Clips an oder ruft diesen ab.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Ruft einen String-Wert ab, der die Version des Windows Media Player angibt.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Gibt einen Wert an, der angibt, ob das Windows Media Player-Steuerelement Video im fensterlosen Modus rendert, oder ruft einen Wert ab.                         |



 

\* Nicht zugänglich für Skins.

Das Player-Objekt unterstützt die folgenden Methoden.



| Methode                                | Beschreibung                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Gibt Windows Media Player Ressourcen frei.                  |
| [launchURL](player-launchurl.md)     | Sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. |
| [Newmedia](player-newmedia.md)       | Erstellt ein neues [Medienobjekt.](media-object.md)           |
| [newPlaylist](player-newplaylist.md) | Erstellt ein neues [Wiedergabelistenobjekt.](playlist-object.md)     |
| [openPlayer](player-openplayer.md)   | Öffnet Windows Media Player unter Verwendung der angegebenen URL.       |



 

Das Player-Objekt unterstützt die folgenden Ereignisse. Ereignisse, die mit einem Sternchen () gekennzeichnet \* sind, sind für Skins nicht zugänglich. Informationen zum Behandeln von Maus- und Tastaturereignissen in Skins finden Sie unter [Externe Ereignisse.](external-events.md)



| Ereignis                                                                                            | Beschreibung                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Tritt ein, wenn sich die aktuelle Audiosprache ändert.                                  |
| [Pufferung](player-player-buffering.md)                                                         | Tritt ein, wenn das Windows Media Player-Steuerelement mit der Pufferung beginnt oder beendet.           |
| [CholeMediaChange](player-player-cdrommediachange.md)                                           | Tritt ein, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird.      |
| [Klicken](player-player-click.md) \*                                                              | Tritt ein, wenn der Benutzer auf eine Maustaste klickt.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Tritt auf, wenn *steuert.* **currentItem-Änderungen.**                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Tritt ein, wenn ein grafisches Metadatenelement im aktuellen Medienelement verfügbar wird. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Tritt ein, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Tritt ein, wenn das aktuelle Wiedergabelistenelement verfügbar wird.                         |
| **Trennen**                                                                                    | Für die zukünftige Verwendung reserviert.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Tritt ein, wenn sich die DVD-Domäne ändert.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Tritt ein, wenn der Benutzer auf eine Maustaste doppelklickt.                               |
| **DurationUnitChange**                                                                           | Für die zukünftige Verwendung reserviert.                                                         |
| **EndOfStream**                                                                                  | Für die zukünftige Verwendung reserviert.                                                         |
| [Fehler](player-player-error.md)                                                                 | Tritt ein, wenn das Windows Media Player-Steuerelement eine Fehlerbedingung aufweist.             |
| [KeyDown](player-player-keydown.md)\*                                                          | Tritt beim Drücken einer Taste ein.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Tritt ein, wenn eine Taste gedrückt und dann losgelassen wird.                                  |
| [KeyUp](player-player-keyup.md)\*                                                              | Tritt ein, wenn eine Taste losgelassen wird.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Tritt ein, wenn ein Marker erreicht wird.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Tritt ein, wenn sich ein Medienelement ändert.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Tritt ein, wenn der Bibliothek ein Attributwert hinzugefügt wird.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Tritt ein, wenn ein Attributwert in der Bibliothek geändert wird.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Tritt ein, wenn ein Attributwert aus der Bibliothek entfernt wird.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Tritt ein, wenn sich die Mediensammlung ändert.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Tritt ein, wenn der lokalen Bibliothek ein Medienelement hinzugefügt wird.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Tritt ein, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Tritt ein, wenn das **Medienobjekt** eine Fehlerbedingung aufweist.                         |
| [ModeChange](player-player-modechange.md)                                                       | Tritt ein, wenn ein Modus von Windows Media Player geändert wird.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Tritt ein, wenn eine Maustaste gedrückt wird.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Tritt ein, wenn der Mauszeiger bewegt wird.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Tritt ein, wenn eine Maustaste losgelassen wird.                                          |
| **NewStream**                                                                                    | Für die zukünftige Verwendung reserviert.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Tritt ein, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Tritt ein, wenn sich der Zustand des Windows Media Player-Steuerelements ändert.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Tritt ein, wenn sich eine Wiedergabeliste ändert.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Tritt ein, wenn sich etwas in der Wiedergabelistenauflistung ändert.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Tritt ein, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Tritt ein, wenn eine Wiedergabeliste aus der Wiedergabelistenauflistung entfernt wird.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Für die zukünftige Verwendung reserviert.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Tritt ein, wenn sich der Wiedergabezustand des Windows Media Player-Steuerelements ändert.          |
| [PositionChange](player-player-positionchange.md)                                               | Tritt ein, wenn die aktuelle Position des Medienelements geändert wurde.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Tritt ein, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Tritt ein, wenn sich der Wert der **Statuseigenschaft** ändert.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Tritt ein, wenn sich eine Zeichenfolgenauflistung ändert.                                         |
| **Warnung**                                                                                      | Für die zukünftige Verwendung reserviert.                                                         |



 

\* Nicht zugänglich für Skins. Informationen zum Behandeln von Maus- und Tastaturereignissen in Skins finden Sie unter [Ambient Event Handlers](ambient-event-handlers.md).

Beim Einbetten in eine Webseite kann auf das **Player-Objekt** mithilfe des id-Werts zugegriffen werden, der im OBJECT-Tag angegeben ist. Innerhalb einer Skindefinitionsdatei erfolgt der  Zugriff über das globale Playerattribut. Zur Veranschaulichung wird **player** als Objekt-ID in den Abschnitten zur Verweissyntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




