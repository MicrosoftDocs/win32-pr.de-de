---
title: Zuordnen und Vorbereiten von MIDI-Datenblöcken
description: Zuordnen und Vorbereiten von MIDI-Datenblöcken
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zuordnen von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Zuordnen von Datenblöcken
- MIDI-Dienste, Zuordnen von Datenblöcken
- Zuordnen von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Vorbereiten von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Vorbereiten von Datenblöcken
- MIDI-Dienste, Vorbereiten von Datenblöcken
- Vorbereiten von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Datenblöcke
- MIDI (Digital Interface Digital Interface), Datenblöcke
- MIDI-Dienste, Datenblöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341717"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Zuordnen und Vorbereiten von MIDI-Datenblöcken

Die Funktionen " [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)", " [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)" und " [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) " erfordern, dass Anwendungen Datenblöcke zuordnen, die für die Wiedergabe oder Aufzeichnung an die Gerätetreiber übergeben werden. Jede dieser Funktionen verwendet eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, um den zugehörigen Datenblock zu beschreiben.

Bevor Sie eine dieser Funktionen verwenden, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie für den Puffer und die Header Struktur, die den Datenblock beschreibt, Arbeitsspeicher zuweisen.

Windows stellt die folgenden Funktionen zum Vorbereiten und Bereinigen von MIDI-Datenblöcken bereit.



| Wert                                                    | Bedeutung                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiinprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Bereitet einen Datenblock für die Eingabe von MIDI vor.                      |
| [**midiinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Bereinigt die Vorbereitung eines MIDI-Eingabedaten Blocks.  |
| [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Bereitet einen MIDI-Ausgabedaten Block vor.                     |
| [**midioutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Bereinigt die Vorbereitung eines MIDI-Ausgabedaten Blocks. |



 

Bevor Sie einen MIDI-Datenblock an einen Gerätetreiber übergeben, müssen Sie den Puffer vorbereiten, indem Sie ihn an die [**midiinprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) -oder [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) -Funktion übergeben. Wenn der Gerätetreiber mit dem Puffer fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigen, indem Sie den Puffer an die [**midiinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) -oder [**midioutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) -Funktion übergeben, bevor zugeordneter Arbeitsspeicher freigegeben werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 