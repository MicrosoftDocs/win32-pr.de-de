---
title: Iagentcharacter
description: Iagentcharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a56272ba095f244e48e335049ec5b88b64855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338212"
---
# <a name="iagentcharacter"></a>Iagentcharacter

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

**Iagentcharacter** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Zeichen Eigenschaften abzufragen und Animationen wiederzugeben. Diese Funktionen sind auch über [**iagentcharakteriex**](iagentcharacterex.md)verfügbar. Sie können einige Methoden Rückgabe Anforderungs-IDs verwenden, um Ihren Status in der Warteschlange des Zeichens zu verfolgen und den Code mit dem aktuellen Animations Zustand des Zeichens zu synchronisieren.

**Methoden in Vtable-Reihenfolge**



| Iagentcharacter-Methoden                                           | BESCHREIBUNG                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Gibt zurück, ob das Zeichen (Frame) momentan sichtbar ist.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Legt die Position des Zeichen Rahmens fest.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Gibt die Position des Zeichen Rahmens zurück.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Legt die Größe des Zeichen Rahmens fest.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Gibt die Größe des Zeichen Rahmens zurück.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Gibt den Namen des Zeichens zurück.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Gibt die Beschreibung für das Zeichen zurück.                                        |
| [**Getttspeed**](iagentcharacter--getttsspeed.md)               | Gibt die aktuelle Einstellung der TTS-Ausgabegeschwindigkeit für das Zeichen zurück.                   |
| [**Getttspitch**](iagentcharacter--getttspitch.md)               | Gibt die aktuelle TTS-Erstellungs Einstellung für das Zeichen zurück.                          |
| [**Aktivieren**](iagentcharacter--activate.md)                     | Legt fest, ob ein Client aktiv ist oder ob ein Zeichen auf oberster Ebene festgelegt ist.                        |
| [**"Abtidleon"**](iagentcharacter--setidleon.md)                   | Legt die Leerlauf Verarbeitung des Servers fest.                                                |
| [**Getidleon**](iagentcharacter--getidleon.md)                   | Gibt die Einstellung der Leerlauf Verarbeitung des Servers zurück.                              |
| [**Vorbereiten**](iagentcharacter--prepare.md)                       | Ruft Animationsdaten für das Zeichen ab.                                       |
| [**Abspielen**](iagentcharacter--play.md)                             | Gibt eine angegebene Animation wieder.                                                      |
| [**Stop**](iagentcharacter--stop.md)                             | Hält eine Animation für ein Zeichen an.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Hält alle Animationen für ein Zeichen an.                                             |
| [**Wait**](iagentcharacter--wait.md)                             | Enthält die Animations Warteschlange des Zeichens.                                            |
| [**Interrupt**](iagentcharacter--interrupt.md)                   | Unterbricht die Animation eines Zeichens.                                               |
| [**Auftritt**](iagentcharacter--show.md)                             | Zeigt das Zeichen an und gibt die Animation **des Zeichen Zustands an** .     |
| [**Ausblenden**](iagentcharacter--hide.md)                             | Gibt die Animation zum **Ausblenden des Zeichens** wieder und blendet den Rahmen des Zeichens aus. |
| [**Speak**](iagentcharacter--speak.md)                           | Gibt eine gesprochene Ausgabe für das Zeichen wieder.                                            |
| [**MoveTo**](iagentcharacter--moveto.md)                         | Verschiebt den Zeichen Rahmen an den angegebenen Speicherort.                              |
| [**Gestureat**](iagentcharacter--gestureat.md)                   | Gibt eine gesturdende Animation basierend auf der angegebenen Position wieder.                      |
| [**Getmuvecause**](iagentcharacter--getmovecause.md)             | Ruft die Ursache für den letzten Verschiebe Vorgang des Zeichens ab.                                 |
| [**Getvisibilitycause**](iagentcharacter--getvisibilitycause.md) | Ruft die Ursache der letzten Änderung des Sichtbarkeits Zustands des Zeichens ab.       |
| [**Hasotherclients**](iagentcharacter--hasotherclients.md)       | Ruft ab, ob das Zeichen über andere aktuelle Clients verfügt.                        |
| [**Setsoundebug**](iagentcharacter--setsoundeffectson.md)   | Bestimmt, ob die Soundeffekte einer Zeichen Animation wiedergegeben werden.                    |
| [**Getsoundebug**](iagentcharacter--getsoundeffectson.md)   | Ruft ab, ob die Einstellung für die Soundeffekte eines Zeichens aktiviert ist.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Legt den Namen des Zeichens fest.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Legt die Beschreibung des Zeichens fest.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Ruft zusätzliche Daten ab, die mit dem-Zeichen gespeichert werden.                              |



 

 

 




