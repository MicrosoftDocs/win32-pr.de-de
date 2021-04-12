---
title: Verwalten der MIDI-Aufzeichnung
description: Verwalten der MIDI-Aufzeichnung
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Digital Instrumentation Digital Interface (MIDI), aufzeichnen
- MIDI (Digital Interface Digital Interface), aufzeichnen
- Aufzeichnen von MIDI-Audiodaten, verwalten
- MIDI-Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472773"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="f85e8-107">Verwalten der MIDI-Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="f85e8-107">Managing MIDI Recording</span></span>

<span data-ttu-id="f85e8-108">Nachdem Sie ein MIDI-Gerät geöffnet haben, können Sie damit beginnen, die Daten von MIDI aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="f85e8-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="f85e8-109">Windows stellt die folgenden Funktionen zum Verwalten der MIDI-Aufzeichnung bereit.</span><span class="sxs-lookup"><span data-stu-id="f85e8-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="f85e8-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f85e8-110">Value</span></span>                                      | <span data-ttu-id="f85e8-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f85e8-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f85e8-112">**midiinaddbuffer**</span><span class="sxs-lookup"><span data-stu-id="f85e8-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="f85e8-113">Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten System exklusiven MIDI-Daten gefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f85e8-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="f85e8-114">**midiinreset**</span><span class="sxs-lookup"><span data-stu-id="f85e8-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="f85e8-115">Beendet die Aufzeichnung von MIDI und markiert alle ausstehenden Puffer als abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f85e8-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="f85e8-116">**midiinstart**</span><span class="sxs-lookup"><span data-stu-id="f85e8-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="f85e8-117">Startet die MIDI-Aufzeichnung und setzt den Zeitstempel auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="f85e8-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="f85e8-118">**midiinstop**</span><span class="sxs-lookup"><span data-stu-id="f85e8-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="f85e8-119">Beendet die Aufzeichnung von MIDI.</span><span class="sxs-lookup"><span data-stu-id="f85e8-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="f85e8-120">Verwenden Sie [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), um Puffer an den Gerätetreiber zum Aufzeichnen von System exklusiven Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="f85e8-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="f85e8-121">Die Anwendung wird benachrichtigt, wenn die Puffer mit System exklusiven aufgezeichneten Daten gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="f85e8-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="f85e8-122">Weitere Informationen zu den Benachrichtigungs Techniken finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="f85e8-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="f85e8-123">Die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion beginnt den Aufzeichnungsprozess.</span><span class="sxs-lookup"><span data-stu-id="f85e8-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="f85e8-124">Wenn Sie System exklusive Nachrichten aufzeichnen, senden Sie mindestens einen Puffer an den Treiber, bevor Sie die Aufzeichnung starten.</span><span class="sxs-lookup"><span data-stu-id="f85e8-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="f85e8-125">Verwenden Sie zum Anhalten der Aufzeichnung [**midiinstop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="f85e8-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="f85e8-126">Markieren Sie vor dem Schließen des Geräts mithilfe der [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) -Funktion alle ausstehenden Datenblöcke als durch den Aufruf von [**midiinreset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="f85e8-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="f85e8-127">Anwendungen, die Zeitstempel Daten benötigen, verwenden eine Rückruffunktion, um die Daten von MIDI zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f85e8-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="f85e8-128">Wenn Ihre Zeit Steuerungsanforderungen nicht strikt sind, können Sie einen Fenster-oder Thread Rückruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="f85e8-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="f85e8-129">Es ist jedoch nicht möglich, einen Ereignis Rückruf zum Empfangen von MIDI-Daten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f85e8-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="f85e8-130">Zum Aufzeichnen von System exklusiven Nachrichten mit Anwendungen, die keine Streampuffer verwenden, müssen Sie den Gerätetreiber mit Puffern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f85e8-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="f85e8-131">Diese Puffer werden mithilfe einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="f85e8-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f85e8-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f85e8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85e8-133">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="f85e8-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 