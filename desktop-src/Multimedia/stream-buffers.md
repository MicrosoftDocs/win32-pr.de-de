---
title: Streampuffer
description: Streampuffer
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimedia,stream buffers
- Multimedia,Streampuffer
- Multimediaaudio, Streampuffer
- Audio,Streampuffer
- Instrument Digital Interface (KEYBOARD), Streampuffer
- KEYBOARD (Instrument Digital Interface, Digitale Schnittstelle des Instrumentalinstruments), Streampuffer
- Streampuffer,About
- KEYBOARDHDR-Struktur
- ENUMERATIONEVENT-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac10d024089a856880097c5d87ae501d62655f858030535ff4128f1fd9d31447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037070"
---
# <a name="stream-buffers"></a>Streampuffer

Anwendungen können Streampuffer verwenden, um Streams von SIGNAL-Ereignissen an ein Gerät zu senden. Jeder Streampuffer ist ein Speicherblock, auf den von einer [**BLOCKHDR-Struktur verwiesen**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) wird. Dieser Speicherblock enthält Daten für ein oder mehrere EVENTS-Ereignisse, die jeweils durch eine [**ENUMERATIONEVENT-Struktur definiert**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) sind. Eine Anwendung steuert den Puffer, indem sie die Streambearbeitungsfunktionen aufruft, z. B. [**"streamStreamOpen",**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen) [**"streamStreamOut"**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)und [**"streamStreamClose".**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)

-   [Streampufferformat](stream-buffer-format.md)
-   [Zeitsteuerungsinformationen](timing-information.md)
-   [EVENTS-Ereignistypen](midi-event-types.md)
-   [KEYBOARD Streams](midi-streams.md)

 

 