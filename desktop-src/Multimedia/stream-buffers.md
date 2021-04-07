---
title: Streampuffer
description: Streampuffer
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows-Multimedia, Streampuffer
- Multimedia, Streampuffer
- Multimedia-Audiodaten, Streampuffer
- Audiodaten, Streampuffer
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Streampuffer, Informationen
- Midihdr-Struktur
- MidiEvent-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725352"
---
# <a name="stream-buffers"></a><span data-ttu-id="1c1f6-112">Streampuffer</span><span class="sxs-lookup"><span data-stu-id="1c1f6-112">Stream Buffers</span></span>

<span data-ttu-id="1c1f6-113">Anwendungen können Streampuffer verwenden, um Datenströme von MIDI-Ereignissen an ein Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="1c1f6-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="1c1f6-114">Jeder Streampuffer ist ein Speicherblock, auf den von einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1c1f6-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="1c1f6-115">Dieser Speicherblock enthält Daten für ein oder mehrere MIDI-Ereignisse, die jeweils durch eine [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c1f6-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="1c1f6-116">Eine Anwendung steuert den Puffer durch Aufrufen der streambearbeitungs Funktionen, wie z. b. [**midistreamopen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)und [**midistreamclose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="1c1f6-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="1c1f6-117">Streampufferformat</span><span class="sxs-lookup"><span data-stu-id="1c1f6-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="1c1f6-118">Informationen zur zeitlichen Steuerung</span><span class="sxs-lookup"><span data-stu-id="1c1f6-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="1c1f6-119">MIDI-Ereignis Typen</span><span class="sxs-lookup"><span data-stu-id="1c1f6-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="1c1f6-120">MIDI-Streams</span><span class="sxs-lookup"><span data-stu-id="1c1f6-120">MIDI Streams</span></span>](midi-streams.md)

 

 