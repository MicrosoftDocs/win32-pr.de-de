---
title: Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe
description: Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Digital Instrumentation Digital Interface (MIDI), gepufferte Wiedergabe
- MIDI (Digital Instrumentation Digital Interface), gepufferte Wiedergabe
- Abspielen von MIDI-Dateien, gepufferte Wiedergabe
- gepufferte Wiedergabe
- MOM_CLOSE Meldung
- MOM_DONE Meldung
- MOM_OPEN Meldung
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), Rückruf Funktionen
- MIDI (Digital Instrumentation Digital Interface), Rückruf Funktionen
- Abspielen von MIDI-Dateien, Rückruf Funktionen
- Midioutproc-Rückruffunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726296"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="6ef13-118">Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="6ef13-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="6ef13-119">Sie können eine eigene Rückruffunktion definieren, um die gepufferte Wiedergabe von MIDI-Ausgabegeräten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6ef13-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="6ef13-120">Die Rückruffunktion ist als [**midioutproc**](/previous-versions//dd798478(v=vs.85))dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6ef13-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="6ef13-121">Die folgenden Meldungen können an den *wmsg* -Parameter der **midioutproc** -Rückruffunktion gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ef13-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="6ef13-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef13-122">Value</span></span>                           | <span data-ttu-id="6ef13-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6ef13-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ef13-124">**MOM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="6ef13-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="6ef13-125">Wird gesendet, wenn das Gerät mit der [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6ef13-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="6ef13-126">**MOM \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="6ef13-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="6ef13-127">Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mit der Funktion [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) oder [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ef13-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="6ef13-128">**MOM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="6ef13-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="6ef13-129">Wird gesendet, wenn das Gerät mit der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6ef13-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="6ef13-130">Diese Nachrichten ähneln denen, die an Fenster Prozedur Funktionen gesendet werden, die Parameter unterscheiden sich jedoch.</span><span class="sxs-lookup"><span data-stu-id="6ef13-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="6ef13-131">Ein Handle des geöffneten MIDI-Geräts wird als Parameter an die Rückruffunktion übergeben, zusammen mit dem Doubleword der mithilfe von **midioutopen** übergebenen Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="6ef13-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="6ef13-132">Nachdem der Treiber mit einem Datenblock fertig ist, können Sie den Datenblock bereinigen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="6ef13-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="6ef13-133">Aufgrund der empfohlenen Einschränkungen für Rückruf Funktionen ist es besser, dies nicht innerhalb der Rückruffunktion durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6ef13-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 