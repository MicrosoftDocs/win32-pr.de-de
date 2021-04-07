---
title: Controls-Objekt
description: Das Steuerelement-Objekt bietet eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu manipulieren.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Steuert Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "103718948"
---
# <a name="controls-object"></a>Controls-Objekt

Das Steuerelement **-Objekt bietet** eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu manipulieren.

Das Steuerelement **-Objekt unterstützt die folgenden** Eigenschaften.



| Eigenschaft                                                            | BESCHREIBUNG                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audiolanguagecount](controls-audiolanguagecount.md)               | Ruft die Anzahl der unterstützten Audiosprachen ab.                                                                                                |
| [currentaudiolanguage](controls-currentaudiolanguage.md)           | Gibt den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.                                                            |
| [currentaudiolanguageindex](controls-currentaudiolanguageindex.md) | Gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.                                                   |
| [currentItem](controls-currentitem.md)                             | Gibt das aktuelle Medien Element an oder ruft es ab.                                                                                                    |
| [currentmarker](controls-currentmarker.md)                         | Gibt die aktuelle Markernummer an oder ruft Sie ab.                                                                                                 |
| [CurrentPosition](controls-currentposition.md)                     | Gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft diese ab.                                                      |
| [currentpositionstring](controls-currentpositionstring.md)         | Ruft die aktuelle Position im Medien Element als **Zeichenfolge** ab.                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Gibt die aktuelle Position im aktuellen Medien Element mithilfe eines Zeit Code Formats an oder ruft diese ab. Diese Eigenschaft unterstützt derzeit den SMPTE-Zeit Code. |
| [isAvailable](controls-isavailable.md)                             | Ruft ab, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.                                                |



 

Das Steuerelement **-Objekt unterstützt die folgenden** Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [FastForward](controls-fastforward.md)                                 | Startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.                                     |
| [fastreverse](controls-fastreverse.md)                                 | Startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.                                     |
| [getaudiolanguagedescription](controls-getaudiolanguagedescription.md) | Ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht. |
| [getaudiolanguageid](controls-getaudiolanguageid.md)                   | Ruft die LCID für einen angegebenen audiosprachindex ab.                                         |
| [getlanguagename](controls-getlanguagename.md)                         | Ruft den Namen der Audiosprache mit der angegebenen LCID ab.                                |
| [Weiter](controls-next.md)                                               | Legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.                                          |
| [pause](controls-pause.md)                                             | Hält die Wiedergabe des Medien Elements an.                                                            |
| [Theater](controls-play.md)                                               | Bewirkt, dass das Medien Element wiedergegeben wird.                                                          |
| [PlayItem](controls-playitem.md)                                       | Bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder setzt die Wiedergabe eines angehaltenen Elements fort.                |
| [previous](controls-previous.md)                                       | Legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.                                      |
| [Schritt](controls-step.md)                                               | Bewirkt, dass das aktuelle Video Medien Element die Wiedergabe im nächsten Frame fixiert.                        |
| [stop](controls-stop.md)                                               | Beendet die Wiedergabe des Medien Elements.                                                             |



 

Der Zugriff auf das Steuerelement Objekt erfolgt **über die folgende** Eigenschaft.



| Object                      | Eigenschaft                        |
|-----------------------------|---------------------------------|
| [Player](player-object.md) | [Steuerelemente](player-controls.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




