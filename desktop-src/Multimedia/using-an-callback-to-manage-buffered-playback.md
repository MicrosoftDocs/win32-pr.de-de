---
title: Verwenden eines Ereignisrückrufs zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Ereignisrückrufs zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Keyboard Instrument Digital Interface (KEYBOARD), gepufferte Wiedergabe
- KEYBOARD (Keyboard Instrument Digital Interface), gepufferte Wiedergabe
- Wiedergeben vonSCHALT-Dateien, gepufferte Wiedergabe
- Gepufferte Wiedergabe
- CreateEvent-Funktion
- Instrument Digital Interface (KEYBOARD), Ereignisrückruf
- KEYBOARD (Instrument Digital Interface), Ereignisrückruf
- Wiedergeben von DANN-Dateien,Ereignisrückruf
- Ereignisrückruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747652c10471662daacfe433a8fc22d5248bf2fe2365b6b314e76d0b91ced127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370266"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Verwenden eines Ereignisrückrufs zum Verwalten der gepufferten Wiedergabe

Um einen Ereignisrückruf zu verwenden, verwenden Sie die [CreateEvent-Funktion,](/windows/win32/api/synchapi/nf-synchapi-createeventa) um das Handle eines Ereignisses abzurufen. Geben Sie in einem Aufruf der [**funktion "keyboardOutOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) CALLBACK \_ EVENT für den *dwFlags-Parameter* an. Erstellen Sie nach der Verwendung der [**Funktion "resetOutPrepareHeader",**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) aber vor dem Senden von ENUMERATION-Ereignissen an das Gerät ein nicht signalisiertes Ereignis, indem Sie die [ResetEvent-Funktion](/windows/win32/api/synchapi/nf-synchapi-resetevent) aufrufen und das von **CreateEvent** abgerufene Ereignishand handle angeben. Verwenden Sie dann in einer Schleife, die überprüft, ob das MHDR \_ DONE-Bit im **dwFlags-Member** der [**EIGENSCHAFTHDR-Struktur festgelegt**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) ist, die [WaitForSingleObject-Funktion,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) und geben Sie das Ereignishandle und den Time out-Wert INFINITE als Parameter an.

Ein Ereignisrückruf wird von allem festgelegt, was einen Funktionsrückruf verursachen kann.

Da Ereignisrückrufe keine spezifischen Benachrichtigungen zum Schließen, Fertig- oder Öffnen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den sie nach dem Auftreten des Ereignisses wartet. Es ist möglich, dass eine Reihe von Aufgaben bis zur Rückgabe von **WaitForSingleObject abgeschlossen** werden kann.

 

 