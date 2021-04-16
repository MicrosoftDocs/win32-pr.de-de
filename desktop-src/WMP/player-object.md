---
title: Player-Objekt
description: Das Player-Objekt ist das Stamm Objekt für das Windows Media Player-Steuerelement. Die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgelistet sind, werden unterstützt.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Player-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104516395"
---
# <a name="player-object"></a>Player-Objekt

Das Player-Objekt ist das Stamm Objekt für das Windows Media Player-Steuerelement. Die Eigenschaften, Methoden und Ereignisse, die in den folgenden Tabellen aufgelistet sind, werden unterstützt.

Das Player-Objekt unterstützt die folgenden Eigenschaften. Eigenschaften, die mit einem Sternchen ( \* ) markiert sind, sind für Skins nicht zugänglich.



| Eigenschaft                                             | BESCHREIBUNG                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromcollection](player-cdromcollection.md)        | Ruft das [cdromcollection](cdromcollection-object.md) -Objekt ab.                                                                          |
| [closedcaption](player-closedcaption.md)            | Ruft das [closedcaption](closedcaption-object.md) -Objekt ab.                                                                              |
| [Steuerelemente](player-controls.md)                      | Ruft [das Steuer](controls-object.md) Element Objekt ab.                                                                                        |
| [currentMedia](player-currentmedia.md)              | Gibt das aktuelle [Medien](media-object.md) Objekt an oder ruft es ab.                                                                         |
| [currentwiedergabe](player-currentplaylist.md)        | Gibt das aktuelle [Wiedergabe](playlist-object.md) Listen Objekt an oder ruft es ab.                                                                   |
| [DVD](player-dvd.md)                                | Ruft das [DVD](dvd-object.md) -Objekt ab.                                                                                                  |
| [enablecontextmenu](player-enablecontextmenu.md)\* | Gibt einen Wert an, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder ruft diesen Wert ab.          |
| [aktiviert](player-enabled.md)\*                     | Gibt einen Wert an, der angibt, ob das Windows Media Player Steuerelement aktiviert ist, oder ruft diesen ab.                                               |
| [error](player-error.md)                            | Ruft das [Fehler](error-object.md) Objekt ab.                                                                                              |
| [Vollbild](player-fullscreen.md)\*               | Gibt einen Wert an, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden, oder ruft ihn ab.                                          |
| [IsOnline](player-isonline.md)                      | Ruft einen Wert ab, der angibt, ob der Benutzer mit einem Netzwerk verbunden ist.                                                                     |
| [IsRemote](player-isremote.md)\*                   | Ruft einen Wert ab, der angibt, ob das Windows Media Player-Steuerelement im Remote Modus ausgeführt wird.                                             |
| [mediacollection](player-mediacollection.md)        | Ruft das [mediacollection](mediacollection-object.md) -Objekt ab.                                                                          |
| [network](player-network.md)                        | Ruft das [Netzwerk](network-object.md) Objekt ab.                                                                                          |
| [openstate](player-openstate.md)                    | Ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.                                                                                |
| [playerapplication](player-playerapplication.md)\* | Ruft das [playerapplication](playerapplication-object.md) -Objekt ab, wenn ein Remotes Windows Media Player-Steuerelement ausgeführt wird.               |
| [playlistcollection](player-playlistcollection.md)  | Ruft das [playlistcollection](playlistcollection-object.md) -Objekt ab.                                                                    |
| [playstate](player-playstate.md)                    | Ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.                                                                |
| [settings](player-settings.md)                      | Ruft das [Einstellungs](settings-object.md) Objekt ab.                                                                                        |
| [status](player-status.md)                          | Ruft einen Wert ab, der den aktuellen Status von Windows-Media Player angibt.                                                                     |
| [stretchdefit](player-stretchtofit.md)\*           | Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob Video auf die Größe der Windows-Media Player Steuerelement-Videoanzeige gestreckt wird          |
| [uiMode](player-uimode.md)\*                       | Gibt einen Wert an, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden, wenn Windows Media Player in eine Webseite eingebettet ist, oder ruft diesen Wert ab. |
| [URL](player-url.md)                                | Gibt den Namen des wieder zugebende Clips an oder ruft ihn ab.                                                                                         |
| [VERSIONINFO](player-versioninfo.md)                | Ruft einen Zeichen folgen Wert ab, der die Version des Windows-Media Player angibt.                                                                 |
| [windowlessvideo](player-windowlessvideo.md)\*     | Gibt einen Wert an, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert, oder ruft diesen ab.                         |



 

\* Der Zugriff auf Skins ist nicht möglich.

Das Player-Objekt unterstützt die folgenden Methoden.



| Methode                                | BESCHREIBUNG                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Gibt Windows Media Player-Ressourcen frei.                  |
| [launchurl](player-launchurl.md)     | Sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. |
| [newmedia](player-newmedia.md)       | Erstellt ein neues [Medien](media-object.md) Objekt.           |
| [neue](player-newplaylist.md) | Erstellt ein neues [Wiedergabe](playlist-object.md) Listen Objekt.     |
| [openplayer](player-openplayer.md)   | Öffnet Windows-Media Player mit der angegebenen URL.       |



 

Das Player-Objekt unterstützt die folgenden Ereignisse. Ereignisse, die mit einem Sternchen ( \* ) markiert sind, sind für Skins nicht zugänglich. Informationen zum Behandeln von Maus-und Tastatur Ereignissen in Skins finden Sie unter [externe Ereignisse](external-events.md).



| Ereignis                                                                                            | BESCHREIBUNG                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Audiolanguagechange](player-player-audiolanguagechange.md)                                     | Tritt auf, wenn sich die aktuelle Audiosprache ändert.                                  |
| [Pufferung](player-player-buffering.md)                                                         | Tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung startet oder beendet.           |
| [Cdrommediachange](player-player-cdrommediachange.md)                                           | Tritt auf, wenn eine CD oder DVD in ein CD-oder DVD-Laufwerk eingefügt oder von dort aus entfernt wird.      |
| [Klicken Sie auf](player-player-click.md)\*                                                              | Tritt ein, wenn der Benutzer auf eine Maustaste klickt.                                      |
| [Ereignis Wechsel](player-player-currentitemchange.md)                                         | Tritt auf, wenn Steuer *Elemente*. das Ereignis **wird geändert.**                                  |
| [Currentmediaitemavailable](player-player-currentmediaitemavailable.md)                         | Tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird. |
| [Currentplaylistchange](player-player-currentplaylistchange.md)                                 | Tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.                       |
| [Currentplaylistitemavailable](player-player-currentplaylistitemavailable.md)                   | Tritt ein, wenn das aktuelle Wiedergabelisten Element verfügbar wird.                         |
| **Disconnect** (Trennen)                                                                                   | Für die zukünftige Verwendung reserviert.                                                         |
| [Domainchange](player-player-domainchange.md)                                                   | Tritt auf, wenn die DVD-Domäne geändert wird.                                              |
| [Doppelklick](player-player-doubleclick.md)\*                                                  | Tritt ein, wenn der Benutzer auf eine Maustaste doppelklickt.                               |
| **Durationunitchange**                                                                           | Für die zukünftige Verwendung reserviert.                                                         |
| **EndOfStream**                                                                                  | Für die zukünftige Verwendung reserviert.                                                         |
| [Fehler](player-player-error.md)                                                                 | Tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.             |
| [KeyDown](player-player-keydown.md)\*                                                          | Tritt beim Drücken einer Taste ein.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Tritt auf, wenn eine Taste gedrückt und anschließend freigegeben wird.                                  |
| [KeyUp](player-player-keyup.md)\*                                                              | Tritt ein, wenn eine Taste losgelassen wird.                                                   |
| [Markerhit](player-player-markerhit.md)                                                         | Tritt ein, wenn ein Marker erreicht wird.                                                 |
| [Mediachange](player-player-mediachange.md)                                                     | Tritt auf, wenn ein Medien Element geändert wird.                                                |
| [Mediacollectionattributestringadded](player-player-mediacollectionattributestringadded.md)     | Tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.                          |
| [Mediacollectionattributestringchanged](player-player-mediacollectionattributestringchanged.md) | Tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.                        |
| [Mediacollectionattributestraningrebewegt](player-player-mediacollectionattributestringremoved.md) | Tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.                      |
| [Mediacollectionchange](player-player-mediacollectionchange.md)                                 | Tritt auf, wenn die Mediensammlung geändert wird.                                        |
| [Mediacollectionmediaadded](player-player-mediacollectionmediaadded.md)                         | Tritt auf, wenn der lokalen Bibliothek ein Medien Element hinzugefügt wird.                          |
| [Mediacollectionmediarebewegt](player-player-mediacollectionmediaremoved.md)                     | Tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.                         |
| [Modeänderung](player-player-modechange.md)                                                       | Tritt auf, wenn ein Windows Media Player-Modus geändert wird.                           |
| [Mouum](player-player-mousedown.md)\*                                                      | Tritt auf, wenn eine Maustaste gedrückt wird.                                           |
| [Mouseelmove](player-player-mousemove.md)\*                                                      | Tritt ein, wenn der Mauszeiger verschoben wird.                                          |
| [Mouberup](player-player-mouseup.md)\*                                                          | Tritt auf, wenn eine Maustaste losgelassen wird.                                          |
| **NewStream**                                                                                    | Für die zukünftige Verwendung reserviert.                                                         |
| [Openplaylistswitch](player-player-openplaylistswitch.md)                                       | Tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Tritt auf, wenn sich der Zustand des Windows Media Player-Steuer Elements ändert                      |
| [Playlistchange](player-player-playlistchange.md)                                               | Tritt auf, wenn eine Wiedergabeliste geändert wird.                                                  |
| [Playlistcollectionchange](player-player-playlistcollectionchange.md)                           | Tritt auf, wenn sich etwas in der Wiedergabelisten Auflistung ändert.                        |
| [Playlistcollectionplaylistadded](player-player-playlistcollectionplaylistadded.md)             | Tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.                      |
| [Playlistcollectionplaylistreverschohe](player-player-playlistcollectionplaylistremoved.md)         | Tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.                  |
| **Playlistcollectionplaylisteintasdeleted**                                                       | Für die zukünftige Verwendung reserviert.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Tritt auf, wenn sich der Wiedergabe Zustand des Windows-Media Player Steuer Elements ändert.          |
| [Positionsänderung](player-player-positionchange.md)                                               | Tritt ein, wenn die aktuelle Position des Medien Elements geändert wurde.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Tritt auf, wenn ein synchronisierter Befehl oder eine URL empfangen wird.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Tritt ein, wenn der Wert der **Status** Eigenschaft geändert wird.                               |
| [Stringcollectionchange](player-player-stringcollectionchange.md)                               | Tritt auf, wenn eine Zeichen folgen Auflistung geändert wird.                                         |
| **Warnung**                                                                                      | Für die zukünftige Verwendung reserviert.                                                         |



 

\* Der Zugriff auf Skins ist nicht möglich. Informationen zum Behandeln von Maus-und Tastatur Ereignissen in Skins finden Sie unter [Ambient-Ereignishandler](ambient-event-handlers.md).

Wenn Sie in eine Webseite eingebettet sind, kann auf das **Player** -Objekt mit dem im Object-Tag angegebenen ID-Wert zugegriffen werden. Innerhalb einer Skin-Definitionsdatei erfolgt der Zugriff mithilfe des globalen Attributs " **Player** ". Zur Veranschaulichung wird **Player** als Objekt-ID in den Abschnitten der Verweis Syntax verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




