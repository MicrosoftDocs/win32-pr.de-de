---
title: Informationen zur zeitlichen Steuerung
description: Informationen zur zeitlichen Steuerung
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zeit Steuerungsinformationen
- MIDI (Digital Instrumentation Digital Interface), Zeit Steuerungsinformationen
- Streampuffer, Zeit Steuerungsinformationen
- MidiEvent-Struktur
- Streampuffer, SMPTE-Format
- Streampuffer, Quartals Hinweis Zeit
- Streampuffer, Ticks
- SMPTE-Format
- Zeit des Quartals Hinweises
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101490"
---
# <a name="timing-information"></a>Informationen zur zeitlichen Steuerung

Zeit Steuerungsinformationen für ein Ereignis vom Typ "MIDI" werden im **dwdelta** -Member der [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur gespeichert. Die Zeit wird in Ticks angegeben, wie in der Standard--Datei mit den- *Standard-Dateien 1,0* definiert. Die Länge eines Teil Strichs wird durch das Uhrzeit Format und möglicherweise vom dem Stream zugeordneten Tempo definiert. Weitere Informationen zu Streams finden Sie unter [MIDI-Streams](midi-streams.md).

Ein Tick wird entweder als Mikrosekunden pro Quartals Notiz oder als Ticks von SMPTE (Society of Motion Picture and TV Engineers)-Zeit ausgedrückt. Anwendungen, die Nachrichten einzeln senden oder nicht verarbeitete MIDI-Nachrichten verwenden, verwenden die Quartals Notiz und die Gültigkeitsdauer eines Teil Strichs. Anwendungen, die eine Vorverarbeitung von MIDI-Nachrichten ausführen, können die verstrichene Zeit als Anzahl der verwendeten SMPTE-Einheiten speichern.

Die Zeit für den Quartals Hinweis wird im Word-Bit (Bit 15) mit einem Nullwert (0) angegeben. Der Rest des Worts enthält den Hinweis Ticks pro Quartal. Ein mit einem Stream von MIDI-Daten verknüpfter Wert wird in Einheiten (Mikrosekunden pro Quartals Notiz) gespeichert, die mit der *Standard mäßigen-Standard-Datei 1,0* -Spezifikation übereinstimmen. Beispiel: ein Quartals Hinweis in 4/4-Zeit, der ein Tempo von 500.000 Mikrosekunden pro Quartals Notiz verwendet, wird mit der Rate von 120 Beats pro Minute abgespielt.

SMPTE-Zeit Abteilungs Formate geben die Länge eines Takts vollständig an, ohne dass die Notwendigkeit von Tempo Informationen erforderlich ist. Bei Verwendung von SMPTE-Zeitformaten können MIDI-Sequenzen mit anderen SMPTE-Ereignissen synchronisiert werden, z. b. Video-oder stripesetaudiodaten. Die SMPTE-Zeit wird mit einem Wert von 1 im höherwertigen Bit (Bit 15) des Zeit Teilungs Worts angegeben. Der Rest des signifikantesten Bytes gibt das verwendete SMPTE-Format als negative Werte an. Die unterstützten SMPTE-Formate und ihre entsprechenden Werte (in Klammern) sind 24 (-24), 25 (-25), 30 (-30) und 30 Drop (-29). Das niedrige Byte des Zeit Teilungs Worts gibt die Anzahl der Ticks pro SMPTE-Rahmen an.

 

 