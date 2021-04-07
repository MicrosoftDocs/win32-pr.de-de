---
title: Streampuffer
description: Streampuffer
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows-Multimedia, Streampuffer
- Multimedia, Streampuffer
- Multimedia-Audiodaten, Streampuffer
- Audiodaten, Streampuffer
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Streampuffer, Informationen
- Midihdr-Struktur
- MidiEvent-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725352"
---
# <a name="stream-buffers"></a>Streampuffer

Anwendungen können Streampuffer verwenden, um Datenströme von MIDI-Ereignissen an ein Gerät zu senden. Jeder Streampuffer ist ein Speicherblock, auf den von einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur verwiesen wird. Dieser Speicherblock enthält Daten für ein oder mehrere MIDI-Ereignisse, die jeweils durch eine [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur definiert werden. Eine Anwendung steuert den Puffer durch Aufrufen der streambearbeitungs Funktionen, wie z. b. [**midistreamopen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)und [**midistreamclose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Streampufferformat](stream-buffer-format.md)
-   [Informationen zur zeitlichen Steuerung](timing-information.md)
-   [MIDI-Ereignis Typen](midi-event-types.md)
-   [MIDI-Streams](midi-streams.md)

 

 