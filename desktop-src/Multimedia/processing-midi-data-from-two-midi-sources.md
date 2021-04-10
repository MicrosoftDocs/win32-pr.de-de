---
title: Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen
description: Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows Multimedia, Verarbeiten von MIDI-Daten aus zwei Quellen
- Multimedia, Verarbeiten von MIDI-Daten aus zwei Quellen
- Multimedia-Audiodaten, Verarbeiten von MIDI-Daten aus zwei Quellen
- Audiodaten, Verarbeiten von MIDI-Daten aus zwei Quellen
- Digital Instrumentation Digital Interface (MIDI), Verarbeiten von Daten aus zwei Quellen
- MIDI (Digital Instrumentation Digital Interface), Verarbeiten von Daten aus zwei Quellen
- Verarbeiten von MIDI-Daten aus zwei Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038924"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen

Das MIDI-Subsystem kann aus zwei Datenquellen aus zwei Datenquellen für die gleichzeitige Wiedergabe an ein einzelnes MIDI-Ausgabegerät weiterleiten. Eine Quelle kann z. b. Hintergrundmusik oder eine Bass Linie sein, die vorab aufgezeichnet und in einer Datei gespeichert wurde. Bei der zweiten Quelle kann es sich um Livedaten aus einem MIDI-Instrument wie Tastatur oder Gitarre handeln.

Beide Datenquellen senden MIDI-Daten an ein einzelnes, mit einem Handle bezeichnetes-Gerät. Senden eines Datenstroms mithilfe der Funktion " [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) " und eines oder mehrerer Streampuffer. Dieser Datenstream enthält normalerweise vorab Daten, die in den Puffer gepackt werden.

Senden Sie den zweiten Datenstrom (in der Regel von einem MIDI-Instrument) mithilfe der [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) -Funktion asynchron. Der laufende Status eines Streampuffers wird von den asynchronen Aufrufen durch den zweiten Datenstrom nicht beeinträchtigt.

Jede mit **midioutshortmsg** gesendete kurze Nachricht muss eine komplette MIDI-Nachricht mit einem Status Byte und der entsprechenden Anzahl von Daten Bytes sein. Wenn das Status Byte ausgelassen wird, gibt **midioutshortmsg** einen Fehler zurück. (Es gibt jedoch keinen ausgegebene Status mit Datenstrom Ausgabe.)

 

 