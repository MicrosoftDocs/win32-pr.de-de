---
title: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Digital Instrumentation Digital Interface (MIDI), gepufferte Wiedergabe
- MIDI (Digital Instrumentation Digital Interface), gepufferte Wiedergabe
- Abspielen von MIDI-Dateien, gepufferte Wiedergabe
- gepufferte Wiedergabe
- MM_MOM_CLOSE Meldung
- MM_MOM_DONE Meldung
- MM_MOM_OPEN Meldung
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315014"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="3f0c4-114">Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="3f0c4-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="3f0c4-115">Die folgenden Meldungen können an ein Fenster oder einen Thread gesendet werden, um die Wiedergabe von System exklusiven Systemnachrichten oder streampuffern zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="3f0c4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3f0c4-116">Value</span></span>                                  | <span data-ttu-id="3f0c4-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f0c4-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f0c4-118">**Schließen von mm \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="3f0c4-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="3f0c4-119">Wird gesendet, wenn das Gerät mit der [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="3f0c4-120">**MM- \_ MOM \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="3f0c4-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="3f0c4-121">Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mit der Funktion [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) oder [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="3f0c4-122">**MM \_ MOM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="3f0c4-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="3f0c4-123">Wird gesendet, wenn das Gerät mit der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="3f0c4-124">Jedem dieser Nachrichten sind ein *wParam* -Parameter und ein *LPARAM* -Parameter zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="3f0c4-125">Der *wParam* -Parameter gibt immer das Handle eines geöffneten MIDI-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="3f0c4-126">Für [**mm \_ MOM \_**](mm-mom-done.md)gibt *LPARAM* eine Adresse einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur an, die den abgeschlossenen Datenblock identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="3f0c4-127">Der *LPARAM* -Parameter wird für [**das \_ \_ Schließen von mm MOM**](mm-mom-close.md) und das [**Öffnen von mm \_ MOM \_**](mm-mom-open.md)nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="3f0c4-128">Die nützlichste Meldung ist wahrscheinlich, dass mm \_ MOM \_ abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="3f0c4-129">Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, ist es wahrscheinlich nicht erforderlich, dass Sie mm \_ MOM \_ Open und mm \_ MOM \_ Close verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="3f0c4-130">Wenn die Wiedergabe eines Datenblocks beendet ist, können Sie den Datenblock bereinigen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="3f0c4-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 