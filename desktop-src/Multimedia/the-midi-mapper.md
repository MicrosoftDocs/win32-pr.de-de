---
title: Der MIDI-Mapper
description: Der MIDI-Mapper
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, MIDI-Mapper
- Multimedia, MIDI-Mapper
- Multimedia-Audiodatei, MIDI-Mapper
- Audiodatei, MIDI-Mapper
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Informationen
- MIDI-Mapper, Quelle
- MIDI-Mapper, Ziel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036788"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="f8dbc-112">Der MIDI-Mapper</span><span class="sxs-lookup"><span data-stu-id="f8dbc-112">The MIDI Mapper</span></span>

<span data-ttu-id="f8dbc-113">Die Standard-patchdienste des MIDI-Mappers stellen eine geräteunabhängige Wiedergabe von MIDI-Dateien für-Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="f8dbc-114">Der MIDI-Mapper kann mit dem MCI-System-und-System-oder-Ausgabe Dienst auf niedriger Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="f8dbc-115">Sofern nicht anders angegeben, verwenden alle Verweise auf die-Nummer des-MIDI-Kanals die logischen Kanalzahlen 1 bis 16.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="f8dbc-116">Diese logischen channelnummern entsprechen den physischen Kanalzahlen 0 bis 15, die tatsächlich Teil der MIDI-Nachricht sind.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="f8dbc-117">Alle Verweise auf die Werte von "MIDI-Programm-ändern" und "Schlüssel" verwenden die physischen Werte 0 bis 127.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="f8dbc-118">Alle Zahlen sind Decimal, es sei denn, es ist ein Präfix "0x" vorangestellt. in diesem Fall sind Sie Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f8dbc-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="f8dbc-119">In der Erörterung der MIDI-Mapper bezieht sich der Begriff *Quelle* auf die Eingabe Seite des MIDI-Mappers.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="f8dbc-120">Der Begriff *Ziel* verweist auf die Ausgabe Seite des MIDI-Mappers.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="f8dbc-121">Ein quellchannel ist beispielsweise der MIDI-Kanal einer Nachricht, die an den MIDI-Mapper gesendet wird, und ein Zielchannel ist der MIDI-Kanal einer Nachricht, die von der MIDI-Mapper an ein Ausgabegerät gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8dbc-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="f8dbc-122">Der MIDI-Mapper und Windows</span><span class="sxs-lookup"><span data-stu-id="f8dbc-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="f8dbc-123">Die Architektur der MIDI-Mapper</span><span class="sxs-lookup"><span data-stu-id="f8dbc-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="f8dbc-124">Die Kanal Zuordnung</span><span class="sxs-lookup"><span data-stu-id="f8dbc-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="f8dbc-125">Patchzuordnungen</span><span class="sxs-lookup"><span data-stu-id="f8dbc-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="f8dbc-126">Volumeskalar</span><span class="sxs-lookup"><span data-stu-id="f8dbc-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="f8dbc-127">Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="f8dbc-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="f8dbc-128">Zusammenfassung der Maps-und MIDI-Meldungen</span><span class="sxs-lookup"><span data-stu-id="f8dbc-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




