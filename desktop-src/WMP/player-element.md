---
title: Player-Element
description: Player-Element
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player Skins, Player-Element
- Skins, Player-Element
- Player-Element
- Verweis für Skins, Player-Element
- Elemente, Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100758"
---
# <a name="player-element"></a>Player-Element

Das **Player** -Element ermöglicht Ihnen das Definieren von Ereignis Handlern und das Angeben der **URL** -Eigenschaft des **Player** -Objekts zur Entwurfszeit in einer Skin-Definitionsdatei. Innerhalb von Skriptcode erfolgt der Zugriff auf das **Player** -Objekt über das globale Attribut des **Players** anstelle eines Namens, der durch ein **ID** -Attribut angegeben wird. Dies wird vom **Player** -Element nicht unterstützt.

Das **Player** -Element unterstützt das folgende Attribut.



| Attribut             | BESCHREIBUNG                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Gibt den Namen der Datei an, die wiedergegeben werden soll, oder ruft ihn ab. |



 

Das **Player** -Element kann Ereignishandler für die folgenden Ereignisse implementieren, die aus dem **Player** -Objekt ausgelöst werden.



| Ereignis                                                                                            | BESCHREIBUNG                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Audiolanguagechange](player-player-audiolanguagechange.md)                                     | Tritt auf, wenn sich die aktuelle Audiosprache ändert.                                  |
| [Pufferung](player-player-buffering.md)                                                         | Tritt auf, wenn Windows Media Player Pufferung startet oder beendet.                       |
| [Cdrommediachange](player-player-cdrommediachange.md)                                           | Tritt auf, wenn das CD-Medium geändert wird.                                                |
| [Ereignis Wechsel](player-player-currentitemchange.md)                                         | Tritt ein, wenn das aktuelle Element geändert wird.                                            |
| [Currentmediaitemavailable](player-player-currentmediaitemavailable.md)                         | Tritt ein, wenn das aktuelle Medien Element verfügbar wird.                            |
| [Currentplaylistchange](player-player-currentplaylistchange.md)                                 | Tritt ein, wenn die aktuelle Wiedergabeliste geändert wird.                                        |
| [Currentplaylistitemavailable](player-player-currentplaylistitemavailable.md)                   | Tritt ein, wenn das aktuelle Wiedergabelisten Element verfügbar wird.                         |
| [Domainchange](player-player-domainchange.md)                                                   | Tritt auf, wenn die DVD-Domäne geändert wird.                                              |
| [Fehler](player-player-error.md)                                                                 | Tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.             |
| [Markerhit](player-player-markerhit.md)                                                         | Tritt auf, wenn ein Windows-Media Player einen Marker im Clip trifft.                |
| [Mediachange](player-player-mediachange.md)                                                     | Tritt auf, wenn ein Medien Element geändert wird.                                                |
| [Mediacollectionattributestringadded](player-player-mediacollectionattributestringadded.md)     | Tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.                          |
| [Mediacollectionattributestringchanged](player-player-mediacollectionattributestringchanged.md) | Tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.                        |
| [Mediacollectionattributestraningrebewegt](player-player-mediacollectionattributestringremoved.md) | Tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.                      |
| [Mediacollectionchange](player-player-mediacollectionchange.md)                                 | Tritt auf, wenn das **mediacollection** -Objekt geändert wird.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Tritt auf, wenn das **Medien** Objekt einen Fehlerzustand aufweist.                         |
| [Modeänderung](player-player-modechange.md)                                                       | Tritt beim Wechseln zwischen dem shuffle-und dem Normalmodus auf.                           |
| [Openplaylistswitch](player-player-openplaylistswitch.md)                                       | Tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Tritt auf, wenn der *Player*. **openstate** -Änderungen.                                      |
| [Playlistchange](player-player-playlistchange.md)                                               | Tritt auf, wenn eine Wiedergabeliste geändert wird.                                                  |
| [Playlistcollectionchange](player-player-playlistcollectionchange.md)                           | Tritt auf, wenn sich etwas in der Wiedergabelisten Auflistung ändert.                        |
| [Playlistcollectionplaylistadded](player-player-playlistcollectionplaylistadded.md)             | Tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.                      |
| [Playlistcollectionplaylistreverschohe](player-player-playlistcollectionplaylistremoved.md)         | Tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Tritt auf, wenn der *Player*. **playstate** ändert sich.                                      |
| [Positionsänderung](player-player-positionchange.md)                                               | Tritt auf, wenn der *Player*. -Steuer *Elemente*. **CurrentPosition** ändert sich.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Tritt auf, wenn Windows Media Player einen in eine Datei eingebetteten Skript Befehl trifft. |
| [StatusChange](player-player-statuschange.md)                                                   | Tritt ein, wenn der Wert der **Status** Eigenschaft geändert wird.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




