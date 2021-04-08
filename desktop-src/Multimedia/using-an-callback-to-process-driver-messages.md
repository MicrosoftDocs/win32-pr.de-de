---
title: Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten
description: Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- Wellenform-Audiodatei, Ereignis Rückruf
- Audiodatenblöcke, Ereignis Rückruf
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Funktion "kreateevent"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725416"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="0c058-109">Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0c058-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="0c058-110">Um einen Ereignis Rückruf zu verwenden, verwenden [**Sie die Funktion**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) "Funktion", um ein manuelles Zurücksetzungs Ereignis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c058-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="0c058-111">Geben Sie im Aufrufen der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion das **Rückruf \_ Ereignis** für den *fdwopen* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0c058-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="0c058-112">Nachdem Sie die [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) -Funktion aufgerufen haben, aber bevor Sie Waveform-Audiodaten an das Gerät gesendet haben, setzen Sie das Ereignis in einen nicht signalisierten Zustand, indem Sie die [**resettevent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0c058-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="0c058-113">Anschließend wird in einer Schleife, die überprüft, ob das **whdr \_ done** -Flag im **dwFlags** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur festgelegt ist, die [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion aufgerufen und als Parameter für das Ereignis Handle und einen Timeout Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="0c058-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="0c058-114">Da Ereignis Rückrufe keine bestimmten Close-, done-oder Open-Benachrichtigungen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0c058-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="0c058-115">Es ist möglich, dass eine Reihe von Aufgaben durch die Rückgabe von [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0c058-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c058-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c058-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c058-117">Audiodatenblöcke</span><span class="sxs-lookup"><span data-stu-id="0c058-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 