---
title: Verwalten von MIDI-Datenblöcken
description: Verwalten von MIDI-Datenblöcken
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Digital Instrumentation Digital Interface (MIDI), Verwalten von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Verwalten von Datenblöcken
- MIDI-Dienste, Verwalten von Datenblöcken
- Verwalten von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Verarbeitung von Treiber Meldungen
- MIDI (Digital Instrumentation Digital Interface), Verarbeiten von Treiber Meldungen
- MIDI-Dienste, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Digital Instrumentation Digital Interface (MIDI), Datenblöcke
- MIDI (Digital Interface Digital Interface), Datenblöcke
- MIDI-Dienste, Datenblöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948634"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="a4fc5-114">Verwalten von MIDI-Datenblöcken</span><span class="sxs-lookup"><span data-stu-id="a4fc5-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="a4fc5-115">Anwendungen, die Datenblöcke zum Übergeben von System exklusiven Nachrichten (mit den Funktionen [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) und [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) und Streampuffer (mithilfe der [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) -Funktion) verwenden, müssen den Gerätetreiber kontinuierlich mit Datenblöcken bereitstellen, bis die Wiedergabe oder Aufzeichnung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="a4fc5-116">Selbst wenn ein einzelner Datenblock verwendet wird, muss eine Anwendung in der Lage sein, zu bestimmen, wann ein Gerätetreiber mit dem Datenblock fertig ist, damit er den dem Datenblock und der Header Struktur zugeordneten Arbeitsspeicher freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="a4fc5-117">Es können drei Methoden verwendet werden, um zu bestimmen, wann ein Gerätetreiber mit einem Datenblock fertiggestellt wird:</span><span class="sxs-lookup"><span data-stu-id="a4fc5-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="a4fc5-118">Geben Sie eine Rückruffunktion an, um eine vom Treiber gesendete Nachricht zu empfangen, wenn Sie mit einem Datenblock fertig ist.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="a4fc5-119">Um die von einem Zeitstempel versehene Daten zu erhalten, müssen Sie eine Rückruffunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="a4fc5-120">Verwenden Sie einen Ereignis Rückruf (nur für die Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="a4fc5-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="a4fc5-121">Verwenden eines Fenster-oder Thread Rückrufs zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn der Vorgang mit einem Datenblock abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="a4fc5-122">Wenn eine Anwendung bei Bedarf keinen Datenblock für den Gerätetreiber erhält, kann eine akustische Lücke bei der Wiedergabe oder ein Verlust eingehender erfasster Informationen auftreten.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="a4fc5-123">Eine Anwendung sollte zumindest ein doppeltes pufferungsschema verwenden, um mindestens einen Datenblock vor dem Gerätetreiber zu behalten.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="a4fc5-124">Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a4fc5-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="a4fc5-125">Sie können eine eigene Rückruffunktion schreiben, um Nachrichten zu verarbeiten, die vom Gerätetreiber gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="a4fc5-126">Um eine Rückruffunktion zu verwenden, geben Sie das Rückruf \_ funktionsflag im *dwFlags* -Parameter und die Adresse der Rückruffunktion im *dwcallback* -Parameter der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -oder [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="a4fc5-127">An eine Rückruffunktion gesendete Nachrichten ähneln Nachrichten, die an ein Fenster gesendet werden, mit dem Unterschied, dass Sie zwei Double Word-Parameter anstelle eines ganzzahligen Parameters ohne Vorzeichen und einen Double Word-Parameter</span><span class="sxs-lookup"><span data-stu-id="a4fc5-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="a4fc5-128">Weitere Informationen zu diesen Nachrichten finden Sie unter [Senden von System-Exclusive Nachrichten](sending-system-exclusive-messages.md) und [Verwalten der MIDI-Aufzeichnung](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="a4fc5-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="a4fc5-129">Verwenden Sie eine der folgenden Verfahren, um Instanzdaten von einer Anwendung an eine Rückruffunktion zu übergeben:</span><span class="sxs-lookup"><span data-stu-id="a4fc5-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="a4fc5-130">Verwenden Sie den *dwcallbackinstance* -Parameter der Funktion, die den Gerätetreiber öffnet.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="a4fc5-131">Verwenden Sie den **DWUser** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, der einen Datenblock identifiziert, der an einen MIDI-Gerätetreiber gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="a4fc5-132">Wenn Sie mehr als 32 Bits von Instanzdaten benötigen, übergeben Sie eine Adresse einer Struktur, die die zusätzlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="a4fc5-133">Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a4fc5-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="a4fc5-134">Um einen Ereignis Rückruf zu verwenden, verwenden Sie die Funktion " [-Funktion", um das Handle](/windows/win32/api/synchapi/nf-synchapi-createeventa) eines Ereignisses abzurufen und das Rückruf \_ Ereignis im Aufrufen der Funktion " [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) " anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="a4fc5-135">Ein Ereignis Rückruf wird durch alle Elemente festgelegt, die einen Funktions Rückruf verursachen könnten.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="a4fc5-136">Anders als Rückruf Funktionen und Fenster-oder Thread Rückrufe empfangen Ereignis Rückrufe keine speziellen Close-, done-oder Open-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="a4fc5-137">Daher muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="a4fc5-138">Weitere Informationen über Ereignis Rückrufe finden Sie unter [Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe](using-an-callback-to-manage-buffered-playback.md).</span><span class="sxs-lookup"><span data-stu-id="a4fc5-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="a4fc5-139">Verwenden eines Fenster-oder Thread Rückrufs zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a4fc5-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="a4fc5-140">Um einen Fenster Rückruf zu verwenden, geben Sie das Rückruf \_ Fenster-Flag im *dwFlags* -Parameter und ein Fenster Handle im nieder wertigen Wort des *dwcallback* -Parameters der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -oder [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="a4fc5-141">Treiber Meldungen werden an die Fenster Prozedur Funktion für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="a4fc5-142">Um einen Thread Rückruf zu verwenden, geben Sie auf ähnliche Weise das Rückruf \_ -threadflag und einen Thread Bezeichner im-Befehl von **midiinopen** oder **midioutopen** an.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="a4fc5-143">In diesem Fall werden Nachrichten anstelle eines Fensters an den angegebenen Thread gesendet.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="a4fc5-144">Nachrichten, die an einen Fenster-oder Thread Rückruf gesendet werden, sind spezifisch für das verwendete MIDI-Gerät.</span><span class="sxs-lookup"><span data-stu-id="a4fc5-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="a4fc5-145">Weitere Informationen zu diesen Nachrichten finden Sie unter [Senden von System-Exclusive Nachrichten](sending-system-exclusive-messages.md) und [Verwalten der MIDI-Aufzeichnung](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="a4fc5-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4fc5-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4fc5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4fc5-147">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="a4fc5-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 