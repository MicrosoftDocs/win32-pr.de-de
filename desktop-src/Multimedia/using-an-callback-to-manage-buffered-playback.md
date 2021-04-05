---
title: Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Digital Instrumentation Digital Interface (MIDI), gepufferte Wiedergabe
- MIDI (Digital Instrumentation Digital Interface), gepufferte Wiedergabe
- Abspielen von MIDI-Dateien, gepufferte Wiedergabe
- gepufferte Wiedergabe
- Funktion "kreateevent"
- Digital Instrumentation Digital Interface (MIDI), Ereignis Rückruf
- MIDI (Digital Interface Digital Interface), Ereignis Rückruf
- Abspielen von MIDI-Dateien, Ereignis Rückruf
- Ereignis Rückruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725417"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe

Um einen Ereignis Rückruf zu verwenden, verwenden Sie die Funktion "-Funktion", [um das Handle](/windows/win32/api/synchapi/nf-synchapi-createeventa) eines Ereignisses abzurufen. Geben Sie in einem Aufrufen der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion \_ das Rückruf Ereignis für den *dwFlags* -Parameter an. Nachdem Sie die [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) -Funktion verwendet haben, aber vor dem Senden von MIDI-Ereignissen an das Gerät, erstellen Sie ein nicht signalisiertes Ereignis, indem Sie die [resettevent](/windows/win32/api/synchapi/nf-synchapi-resetevent) -Funktion aufrufen und das von **CreateEvent** abgerufene Ereignis Handle angeben. Verwenden Sie dann in einer Schleife, die überprüft, ob das MHDR \_ done-Bit im **dwFlags** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur festgelegt ist, die [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion, wobei das Ereignis Handle und der Timeout Wert Infinite als Parameter angegeben werden.

Ein Ereignis Rückruf wird durch alle Elemente festgelegt, die einen Funktions Rückruf verursachen könnten.

Da Ereignis Rückrufe keine bestimmten Close-, done-oder Open-Benachrichtigungen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist. Möglicherweise kann eine Reihe von Aufgaben durch die Rückgabe von **WaitForSingleObject** abgeschlossen werden.

 

 