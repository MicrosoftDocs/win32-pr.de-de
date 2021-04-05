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
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="ff50d-112">Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="ff50d-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="ff50d-113">Um einen Ereignis Rückruf zu verwenden, verwenden Sie die Funktion "-Funktion", [um das Handle](/windows/win32/api/synchapi/nf-synchapi-createeventa) eines Ereignisses abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff50d-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="ff50d-114">Geben Sie in einem Aufrufen der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion \_ das Rückruf Ereignis für den *dwFlags* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ff50d-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="ff50d-115">Nachdem Sie die [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) -Funktion verwendet haben, aber vor dem Senden von MIDI-Ereignissen an das Gerät, erstellen Sie ein nicht signalisiertes Ereignis, indem Sie die [resettevent](/windows/win32/api/synchapi/nf-synchapi-resetevent) -Funktion aufrufen und das von **CreateEvent** abgerufene Ereignis Handle angeben.</span><span class="sxs-lookup"><span data-stu-id="ff50d-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="ff50d-116">Verwenden Sie dann in einer Schleife, die überprüft, ob das MHDR \_ done-Bit im **dwFlags** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur festgelegt ist, die [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion, wobei das Ereignis Handle und der Timeout Wert Infinite als Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff50d-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="ff50d-117">Ein Ereignis Rückruf wird durch alle Elemente festgelegt, die einen Funktions Rückruf verursachen könnten.</span><span class="sxs-lookup"><span data-stu-id="ff50d-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="ff50d-118">Da Ereignis Rückrufe keine bestimmten Close-, done-oder Open-Benachrichtigungen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ff50d-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="ff50d-119">Möglicherweise kann eine Reihe von Aufgaben durch die Rückgabe von **WaitForSingleObject** abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ff50d-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 