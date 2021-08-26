---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7144c6d3379a2237d3f14c955d8052ff4d20d1ff98d9c2f2637796f8b931b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962090"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

**IAgentCharacter definiert eine** Schnittstelle, mit der Anwendungen Zeicheneigenschaften abfragen und Animationen wieder geben können. Diese Funktionen sind auch über [**IAgentCharacterEx verfügbar.**](iagentcharacterex.md) Sie können einige Methoden-Rückgabeanforderungs-IDs verwenden, um ihren Status in der Warteschlange des Zeichens zu verfolgen und Ihren Code mit dem aktuellen Animationszustand des Zeichens zu synchronisieren.

**Methoden in Vtable-Reihenfolge**



| IAgentCharacter-Methoden                                           | Beschreibung                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**Getvisible**](iagentcharacter--getvisible.md)                 | Gibt zurück, ob das Zeichen (Frame) derzeit sichtbar ist.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Legt die Position des Zeichenrahmens fest.                                         |
| [**Getposition**](iagentcharacter--getposition.md)               | Gibt die Position des Zeichenrahmens zurück.                                      |
| [**Setsize**](iagentcharacter--setsize.md)                       | Legt die Größe des Zeichenrahmens fest.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Gibt die Größe des Zeichenrahmens zurück.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Gibt den Namen des Zeichens zurück.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Gibt die Beschreibung für das Zeichen zurück.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Gibt die aktuelle TTS-Ausgabegeschwindigkeit für das Zeichen zurück.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Gibt die aktuelle TTS-Tonhöheneinstellung für das Zeichen zurück.                          |
| [**Aktivieren**](iagentcharacter--activate.md)                     | Legt fest, ob ein Client aktiv oder ein Zeichen ganz oben ist.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Legt die Verarbeitung des Servers im Leerlauf fest.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Gibt die Einstellung der Verarbeitung des Servers im Leerlauf zurück.                              |
| [**Vorbereiten**](iagentcharacter--prepare.md)                       | Ruft Animationsdaten für das Zeichen ab.                                       |
| [**Abspielen**](iagentcharacter--play.md)                             | Gibt eine angegebene Animation wieder.                                                      |
| [**Beenden**](iagentcharacter--stop.md)                             | Beendet eine Animation für ein Zeichen.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Beendet alle Animationen für ein Zeichen.                                             |
| [**Wait**](iagentcharacter--wait.md)                             | Enthält die Animationswarteschlange des Zeichens.                                            |
| [**Interrupt**](iagentcharacter--interrupt.md)                   | Unterbricht die Animation eines Zeichens.                                               |
| [**Zeigen**](iagentcharacter--show.md)                             | Zeigt das Zeichen an und gibt die Animation Status anzeigen des **Zeichens** wieder.     |
| [**Ausblenden**](iagentcharacter--hide.md)                             | Gibt die **Hiding-Zustandsanimation** des Zeichens wieder und blendet den Rahmen des Zeichens aus. |
| [**Speak**](iagentcharacter--speak.md)                           | Gibt die gesprochene Ausgabe für das Zeichen wieder.                                            |
| [**Moveto**](iagentcharacter--moveto.md)                         | Verschiebt den Zeichenrahmen an die angegebene Position.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Gibt eine Gesturierungsanimation basierend auf der angegebenen Position wieder.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Ruft die Ursache der letzten Bewegung des Zeichens ab.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Ruft die Ursache der letzten Änderung des Sichtbarkeitszustands des Zeichens ab.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Ruft ab, ob das Zeichen über andere aktuelle Clients verfügt.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Bestimmt, ob die Soundeffekte einer Zeichenanimation wiederklangen.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Ruft ab, ob die Einstellung für Soundeffekte eines Zeichens aktiviert ist.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Legt den Namen des Zeichens fest.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Legt die Beschreibung des Zeichens fest.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Ruft zusätzliche Daten ab, die mit dem Zeichen gespeichert sind.                              |



 

 

 




