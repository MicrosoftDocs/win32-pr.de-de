---
title: Verwenden von midioutshortmsg zum Senden einzelner MIDI-Nachrichten
description: Verwenden von midioutshortmsg zum Senden einzelner MIDI-Nachrichten
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), midioutshortmsg-Funktion
- MIDI (Digital Instrumentation Digital Interface), midioutshortmsg-Funktion
- midioutshortmsg-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472973"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Verwenden von midioutshortmsg zum Senden einzelner MIDI-Nachrichten

Im folgenden Beispiel wird die [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) -Funktion verwendet, um ein angegebenes MIDI-Ereignis an ein bestimmtes MIDI-Ausgabegerät zu senden:


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> Zum Überprüfen von Daten vor dem Senden an einen Ausgabeport sind keine MIDI-Ausgabetreiber erforderlich. Anwendungen müssen sicherstellen, dass nur gültige Daten gesendet werden.

 

 

 