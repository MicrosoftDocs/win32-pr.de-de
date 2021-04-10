---
title: MIDI-Ereignis Typen
description: MIDI-Ereignis Typen
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ereignis Typen
- MIDI (Digital Instrumentation Digital Interface), Ereignis Typen
- MidiEvent-Struktur
- Streampuffer, MIDI-Ereignis Typen
- MIDI-Ereignis Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038969"
---
# <a name="midi-event-types"></a><span data-ttu-id="8e1b6-108">MIDI-Ereignis Typen</span><span class="sxs-lookup"><span data-stu-id="8e1b6-108">MIDI Event Types</span></span>

<span data-ttu-id="8e1b6-109">Der **dwevent** -Member der [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur beschreibt das zu durch zuwählenden MIDI-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="8e1b6-110">Kurze Ereignisse sind vollständig in diesen Member integriert.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="8e1b6-111">Lange Ereignisse erfordern zusätzlich zum **dwevent** -Member einen oder mehrere Double Word-Werte, um die Ereignis Beschreibungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="8e1b6-112">Das hohe Byte des **dwevent** -Members enthält Informationen darüber, ob das Ereignis lang oder kurz ist, und ob ein Rückruf zusammen mit dem Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="8e1b6-113">Außerdem wird dieses Byte verwendet, um den Ereignistyp zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="8e1b6-114">Die verbleibenden 24 Bits des **dwevent** -Members werden entweder verwendet, um die Ereignis Parameter (für kurze Nachrichten) oder die Länge der Ereignis Parameter (für lange Nachrichten) zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="8e1b6-115">Um Informationen aus dem **dwevent** -Member zu extrahieren, verwenden Sie den [**mevt \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) -und [**mevt \_ eventarm**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) -Makros.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="8e1b6-116">Eine Beschreibung der vordefinierten Ereignis Typen finden Sie im Referenzmaterial für die **MidiEvent** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8e1b6-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 