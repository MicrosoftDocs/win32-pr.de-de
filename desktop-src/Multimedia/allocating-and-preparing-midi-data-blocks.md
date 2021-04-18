---
title: Zuordnen und Vorbereiten von MIDI-Datenblöcken
description: Zuordnen und Vorbereiten von MIDI-Datenblöcken
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zuordnen von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Zuordnen von Datenblöcken
- MIDI-Dienste, Zuordnen von Datenblöcken
- Zuordnen von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Vorbereiten von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Vorbereiten von Datenblöcken
- MIDI-Dienste, Vorbereiten von Datenblöcken
- Vorbereiten von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Datenblöcke
- MIDI (Digital Interface Digital Interface), Datenblöcke
- MIDI-Dienste, Datenblöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341717"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="ee5b0-114">Zuordnen und Vorbereiten von MIDI-Datenblöcken</span><span class="sxs-lookup"><span data-stu-id="ee5b0-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="ee5b0-115">Die Funktionen " [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)", " [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)" und " [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) " erfordern, dass Anwendungen Datenblöcke zuordnen, die für die Wiedergabe oder Aufzeichnung an die Gerätetreiber übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="ee5b0-116">Jede dieser Funktionen verwendet eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, um den zugehörigen Datenblock zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="ee5b0-117">Bevor Sie eine dieser Funktionen verwenden, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie für den Puffer und die Header Struktur, die den Datenblock beschreibt, Arbeitsspeicher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="ee5b0-118">Windows stellt die folgenden Funktionen zum Vorbereiten und Bereinigen von MIDI-Datenblöcken bereit.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="ee5b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ee5b0-119">Value</span></span>                                                    | <span data-ttu-id="ee5b0-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ee5b0-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ee5b0-121">**midiinprepareheader**</span><span class="sxs-lookup"><span data-stu-id="ee5b0-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="ee5b0-122">Bereitet einen Datenblock für die Eingabe von MIDI vor.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="ee5b0-123">**midiinunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="ee5b0-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="ee5b0-124">Bereinigt die Vorbereitung eines MIDI-Eingabedaten Blocks.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="ee5b0-125">**midioutprepareheader**</span><span class="sxs-lookup"><span data-stu-id="ee5b0-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="ee5b0-126">Bereitet einen MIDI-Ausgabedaten Block vor.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="ee5b0-127">**midioutunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="ee5b0-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="ee5b0-128">Bereinigt die Vorbereitung eines MIDI-Ausgabedaten Blocks.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="ee5b0-129">Bevor Sie einen MIDI-Datenblock an einen Gerätetreiber übergeben, müssen Sie den Puffer vorbereiten, indem Sie ihn an die [**midiinprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) -oder [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="ee5b0-130">Wenn der Gerätetreiber mit dem Puffer fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigen, indem Sie den Puffer an die [**midiinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) -oder [**midioutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) -Funktion übergeben, bevor zugeordneter Arbeitsspeicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee5b0-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee5b0-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee5b0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee5b0-132">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="ee5b0-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 