---
title: Die Kanal Zuordnung
description: Die Kanal Zuordnung
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Kanal Zuordnung
- Kanal Zuordnung
- MIDI-Mapper, Kanalnachrichten
- MIDI-Kanal Meldungen
- Kanal Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100751"
---
# <a name="the-channel-map"></a><span data-ttu-id="d7cb7-110">Die Kanal Zuordnung</span><span class="sxs-lookup"><span data-stu-id="d7cb7-110">The Channel Map</span></span>

<span data-ttu-id="d7cb7-111">Die Kanal Zuordnung wirkt sich auf alle MIDI-Kanalnachrichten aus.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="d7cb7-112">Zu den Nachrichten von MIDI-Kanälen gehören Notiz-on, Note-Off, polyonic-after-afterberührungs, Steuerelement Änderung, Programmänderung, Channel-afterberührungs-und Nachrichten-Änderungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="d7cb7-113">Der MIDI-Mapper verwendet eine einzelne Kanal Zuordnung mit einem Eintrag für jeden der 16 MIDI-Kanäle.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="d7cb7-114">Jeder Kanal Zuordnungs Eintrag gibt Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="d7cb7-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="d7cb7-115">Ein Zielchannel für die MIDI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="d7cb7-116">Ein Ziel Ausgabegerät für die MIDI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7cb7-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="d7cb7-117">Eine optionale patchkarte, die andere mögliche Änderungen für die MIDI-Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="d7cb7-118">Der Zielchannel ist auf einen der 16 MIDI-Kanäle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="d7cb7-119">Die Nachrichten werden für die einzelnen neuen Kanal Zuweisungen geändert.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="d7cb7-120">Wenn z. b. der Ziel Kanal Eintrag für den MIDI-Kanal 4 auf 6 festgelegt ist, werden alle an Channel 4 gesendeten MIDI-Nachrichten Channel 6 zugeordnet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![zugeordnetes-](images/mmap-a05.gif)

<span data-ttu-id="d7cb7-122">In diesem Beispiel ist das MIDI-Status Byte 0x93 0x95 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="d7cb7-123">Die niedrige Reihenfolge eines "MIDI Status Byte" gibt die Nummer des Kanals an.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="d7cb7-124">Quell Kanäle werden entweder auf "aktiv" oder "inaktiv" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="d7cb7-125">An inaktive Quell Kanäle gesendete Nachrichten werden ignoriert, sodass ein inaktiver Kanal in Kraft tritt oder ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="d7cb7-126">Das Ziel Ausgabegerät ist auf eines der verfügbaren MIDI-Ausgabegeräte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="d7cb7-127">Bei einem Ausgabegerät vom Typ "MIDI" kann es sich um einen internen Synthesizer oder einen physischen, von einem Port</span><span class="sxs-lookup"><span data-stu-id="d7cb7-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="d7cb7-128">Bei den Systemnachrichten von System-/0xF0-und 0xFF-Meldungen handelt es sich um eine MIDI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7cb7-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="d7cb7-129">Es ist kein Kanal mit den Systemnachrichten von MIDI verknüpft und kann daher nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="d7cb7-130">MIDI-Systemmeldungen werden an alle in einer Kanal Zuordnung aufgeführten in einer Kanal Zuordnung aufgeführten in einer Kanal Zuordnung aufgeführten-</span><span class="sxs-lookup"><span data-stu-id="d7cb7-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




