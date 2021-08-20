---
title: PLAYER-Element
description: PLAYER-Element
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player,PLAYER-Element
- skins,PLAYER-Element
- PLAYER-Element
- Referenz für Skins, PLAYER-Element
- Elements,PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bef2e7758a0146ae6197d17dc3790011a758f9d2fa4e3d54af9461a8b870c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338116"
---
# <a name="player-element"></a>PLAYER-Element

Mit **dem PLAYER-Element** können Sie Ereignishandler definieren und die **URL-Eigenschaft** des **Player-Objekts** zur Entwurfszeit in einer Skindefinitionsdatei angeben. Innerhalb des Skriptcodes erfolgt der  Zugriff auf das **Player-Objekt** über das globale Player-Attribut und nicht über einen Namen, der durch ein **ID-Attribut** angegeben wird, was vom **PLAYER-Element nicht unterstützt** wird.

Das **PLAYER-Element** unterstützt das folgende Attribut.



| attribute             | BESCHREIBUNG                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Gibt den Namen der datei an, die abspielt werden soll, oder ruft sie ab. |



 

Das **PLAYER-Element** kann Ereignishandler für die folgenden Ereignisse implementieren, die vom **Player-Objekt ausgelöst** werden.



| Ereignis                                                                                            | Beschreibung                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Tritt ein, wenn sich die aktuelle Audiosprache ändert.                                  |
| [Pufferung](player-player-buffering.md)                                                         | Tritt ein, wenn Windows Media Player Pufferung beginnt oder beendet.                       |
| [CmediaChange](player-player-cdrommediachange.md)                                           | Tritt auf, wenn sich das CD-Medium ändert.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Tritt ein, wenn sich das aktuelle Element ändert.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Tritt ein, wenn das aktuelle Medienelement verfügbar wird.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Tritt ein, wenn sich die aktuelle Wiedergabeliste ändert.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Tritt ein, wenn das aktuelle Wiedergabelistenelement verfügbar wird.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Tritt ein, wenn sich die DVD-Domäne ändert.                                              |
| [Fehler](player-player-error.md)                                                                 | Tritt ein, wenn das Windows Media Player-Steuerelement eine Fehlerbedingung auf hat.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Tritt ein, Windows Media Player im Clip auf einen Marker trifft.                |
| [MediaChange](player-player-mediachange.md)                                                     | Tritt ein, wenn sich ein Medienelement ändert.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Tritt ein, wenn der Bibliothek ein Attributwert hinzugefügt wird.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Tritt ein, wenn ein Attributwert in der Bibliothek geändert wird.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Tritt ein, wenn ein Attributwert aus der Bibliothek entfernt wird.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Tritt ein, wenn sich **das MediaCollection-Objekt** ändert.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Tritt auf, wenn das **Media-Objekt** eine Fehlerbedingung auf hat.                         |
| [ModeChange](player-player-modechange.md)                                                       | Tritt beim Wechseln zwischen Shuffle und normalem Modus auf.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Tritt ein, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Tritt auf, wenn *player*. **openState-Änderungen.**                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Tritt ein, wenn sich eine Wiedergabeliste ändert.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Tritt ein, wenn sich etwas in der Wiedergabelistensammlung ändert.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Tritt ein, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Tritt ein, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Tritt auf, wenn *player*. **playState-Änderungen.**                                      |
| [PositionChange](player-player-positionchange.md)                                               | Tritt auf, wenn *player*. *steuert*. **currentPosition** ändert sich.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Tritt ein, Windows Media Player ein skriptbefehl in eine Datei eingebettet wird. |
| [StatusChange](player-player-statuschange.md)                                                   | Tritt ein, wenn **die Statuseigenschaft** den Wert ändert.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




