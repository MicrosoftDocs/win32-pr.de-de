---
title: Verwenden eines Ereignisrückrufs zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Ereignisrückrufs zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Music Instrument Digital Interface (OPC), gepufferte Wiedergabe
- INSTRUMENTS (Music Instrument Digital Interface),gepufferte Wiedergabe
- Wiedergabe von WIEDERGABEDATEIEN, gepufferte Wiedergabe
- Gepufferte Wiedergabe
- CreateEvent-Funktion
- Music Instrument Digital Interface (OPC), Ereignisrückruf
- INSTRUMENTS (Music Instrument Digital Interface), Ereignisrückruf
- Wiedergeben von TEXTDATEI-Dateien, Ereignisrückruf
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

Um einen Ereignisrückruf zu verwenden, verwenden Sie die [CreateEvent-Funktion,](/windows/win32/api/synchapi/nf-synchapi-createeventa) um das Handle eines Ereignisses abzurufen. Geben Sie in einem Aufruf der [**funktion "dwOutOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) CALLBACK \_ EVENT für den *dwFlags-Parameter* an. Erstellen Sie nach der Verwendung der [**funktion "resetOutPrepareHeader"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) und vor dem Senden von EREIGNISSEN an das Gerät ein nicht signalisiertes Ereignis, indem Sie die [ResetEvent-Funktion](/windows/win32/api/synchapi/nf-synchapi-resetevent) aufrufen und das ereignishandle angeben, das von **CreateEvent** abgerufen wurde. Verwenden Sie dann innerhalb einer Schleife, die überprüft, ob das MHDR \_ DONE-Bit im **dwFlags-Member** der [**CABHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) festgelegt ist, die [WaitForSingleObject-Funktion,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) und geben Sie das Ereignishandle und einen Time out-Wert infinite als Parameter an.

Ein Ereignisrückruf wird durch alles festgelegt, was einen Funktionsrückruf verursachen kann.

Da Ereignisrückrufe keine bestimmten Benachrichtigungen zum Schließen, Fertigstellen oder Öffnen erhalten, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den sie wartet, nachdem das Ereignis aufgetreten ist. Es ist möglich, dass eine Reihe von Aufgaben bis zum Zeitpunkt abgeschlossen werden kann, zu dem **WaitForSingleObject** zurückgegeben wird.

 

 