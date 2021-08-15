---
title: Controls-Objekt
description: Das Controls-Objekt bietet eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu bearbeiten.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Controls-Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 089524750d670c8f4d11aefbfb5993586d9b8a1b0ecfddb3b13316d92243e411
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936696"
---
# <a name="controls-object"></a>Controls-Objekt

Das **Controls-Objekt** bietet eine Möglichkeit, die Wiedergabe von Medien mithilfe der folgenden Eigenschaften und Methoden zu bearbeiten.

Das **Controls-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                                            | BESCHREIBUNG                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | Ruft die Anzahl der unterstützten Audiosprachen ab.                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | Gibt den Locale Identifier (LCID) der Audiosprache für die Wiedergabe an oder ruft diese ab.                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | Gibt den einbasierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft diesen ab.                                                   |
| [Currentitem](controls-currentitem.md)                             | Gibt das aktuelle Medienelement an oder ruft es ab.                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | Gibt die aktuelle Markernummer an oder ruft sie ab.                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | Gibt die aktuelle Position im Medienelement in Sekunden ab dem Anfang an oder ruft sie ab.                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | Ruft die aktuelle Position im Medienelement als Zeichenfolge **ab.**                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Gibt die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats an oder ruft sie ab. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode. |
| [Isavailable](controls-isavailable.md)                             | Ruft ab, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.                                                |



 

Das **Controls-Objekt** unterstützt die folgenden Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Fastforward](controls-fastforward.md)                                 | Startet die schnelle Wiedergabe des Medienelements in Vorwärtsrichtung.                                     |
| [fastReverse](controls-fastreverse.md)                                 | Startet die schnelle Wiedergabe des Medienelements in umgekehrter Richtung.                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | Ruft die Beschreibung für die Audiosprache ab, die dem angegebenen einbasierten Index entspricht. |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | Ruft die LCID für einen angegebenen Audiosprachindex ab.                                         |
| [getLanguageName](controls-getlanguagename.md)                         | Ruft den Namen der Audiosprache mit der angegebenen LCID ab.                                |
| [Weiter](controls-next.md)                                               | Legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.                                          |
| [pause](controls-pause.md)                                             | Hält die Wiedergabe des Medienelements an.                                                            |
| [Spielen](controls-play.md)                                               | Bewirkt, dass das Medienelement abspielt.                                                          |
| [playItem](controls-playitem.md)                                       | Bewirkt, dass die Wiedergabe des aktuellen Medienelements beginnt oder die Wiedergabe eines angehaltenen Elements fortgesetzt wird.                |
| [previous](controls-previous.md)                                       | Legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.                                      |
| [Schritt](controls-step.md)                                               | Bewirkt, dass das aktuelle Videomedienelement die Wiedergabe auf dem nächsten Frame einfriert.                        |
| [stop](controls-stop.md)                                               | Beendet die Wiedergabe des Medienelements.                                                             |



 

Auf **das Controls-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                        |
|-----------------------------|---------------------------------|
| [Player](player-object.md) | [Steuerelemente](player-controls.md) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




