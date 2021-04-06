---
title: MIDI-Streams
description: MIDI-Streams
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Digital Instrumentation Digital Interface (MIDI), Streams
- MIDI (Digital Instrumentation Digital Interface), Streams
- Streampuffer, MIDI-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101595"
---
# <a name="midi-streams"></a>MIDI-Streams

MIDI-Ereignisse treten im Zusammenhang mit einem Stream von MIDI-Daten auf. Obwohl eine Anwendung mehrere Streams zum Definieren von musikalischen Daten verwenden kann, erkennt der MIDI-Mapper nicht mehrere Datenströme. Die meisten Anwendungen, die Streams verwenden, verwenden einen einzelnen Datenstrom.

Die folgenden Funktionen können mit Streams verwendet werden.



| Wert                                            | Bedeutung                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midistreamclose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Schließt einen MIDI-Stream.                                                   |
| [**midistreamopen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Öffnet einen MIDI-Stream und ruft ein Handle ab.                             |
| [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Gibt einen Datenstrom (Puffer) von "MIDI"-Daten in einem MIDI-Ausgabegerät an |
| [**midistreampause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Hält die Wiedergabe eines angegebenen MIDI-Streams an.                             |
| [**midistreamposition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Ruft die aktuelle Position in einem MIDI-Stream ab.                        |
| [**midistreamproperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Legt die streameigenschaften fest und ruft Sie ab.                                   |
| [**midistreamrestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Startet die Wiedergabe eines angehaltenen MIDI-Datenstroms neu.                              |
| [**midistreamstoppt**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Deaktiviert alle Notizen für alle MIDI-Kanäle für den angegebenen MIDI-Stream. |



 

 

 