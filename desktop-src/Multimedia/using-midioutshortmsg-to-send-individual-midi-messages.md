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
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a><span data-ttu-id="98e9f-109">Verwenden von midioutshortmsg zum Senden einzelner MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="98e9f-109">Using midiOutShortMsg to Send Individual MIDI Messages</span></span>

<span data-ttu-id="98e9f-110">Im folgenden Beispiel wird die [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) -Funktion verwendet, um ein angegebenes MIDI-Ereignis an ein bestimmtes MIDI-Ausgabegerät zu senden:</span><span class="sxs-lookup"><span data-stu-id="98e9f-110">The following example uses the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function to send a specified MIDI event to a given MIDI output device:</span></span>


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
> <span data-ttu-id="98e9f-111">Zum Überprüfen von Daten vor dem Senden an einen Ausgabeport sind keine MIDI-Ausgabetreiber erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98e9f-111">MIDI output drivers are not required to verify data before sending it to an output port.</span></span> <span data-ttu-id="98e9f-112">Anwendungen müssen sicherstellen, dass nur gültige Daten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="98e9f-112">Applications must ensure that only valid data is sent.</span></span>

 

 

 