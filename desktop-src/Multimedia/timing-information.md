---
title: Informationen zur zeitlichen Steuerung
description: Informationen zur zeitlichen Steuerung
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zeit Steuerungsinformationen
- MIDI (Digital Instrumentation Digital Interface), Zeit Steuerungsinformationen
- Streampuffer, Zeit Steuerungsinformationen
- MidiEvent-Struktur
- Streampuffer, SMPTE-Format
- Streampuffer, Quartals Hinweis Zeit
- Streampuffer, Ticks
- SMPTE-Format
- Zeit des Quartals Hinweises
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101490"
---
# <a name="timing-information"></a><span data-ttu-id="88c00-113">Informationen zur zeitlichen Steuerung</span><span class="sxs-lookup"><span data-stu-id="88c00-113">Timing Information</span></span>

<span data-ttu-id="88c00-114">Zeit Steuerungsinformationen für ein Ereignis vom Typ "MIDI" werden im **dwdelta** -Member der [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88c00-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="88c00-115">Die Zeit wird in Ticks angegeben, wie in der Standard--Datei mit den- *Standard-Dateien 1,0* definiert.</span><span class="sxs-lookup"><span data-stu-id="88c00-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="88c00-116">Die Länge eines Teil Strichs wird durch das Uhrzeit Format und möglicherweise vom dem Stream zugeordneten Tempo definiert.</span><span class="sxs-lookup"><span data-stu-id="88c00-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="88c00-117">Weitere Informationen zu Streams finden Sie unter [MIDI-Streams](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="88c00-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="88c00-118">Ein Tick wird entweder als Mikrosekunden pro Quartals Notiz oder als Ticks von SMPTE (Society of Motion Picture and TV Engineers)-Zeit ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="88c00-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="88c00-119">Anwendungen, die Nachrichten einzeln senden oder nicht verarbeitete MIDI-Nachrichten verwenden, verwenden die Quartals Notiz und die Gültigkeitsdauer eines Teil Strichs.</span><span class="sxs-lookup"><span data-stu-id="88c00-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="88c00-120">Anwendungen, die eine Vorverarbeitung von MIDI-Nachrichten ausführen, können die verstrichene Zeit als Anzahl der verwendeten SMPTE-Einheiten speichern.</span><span class="sxs-lookup"><span data-stu-id="88c00-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="88c00-121">Die Zeit für den Quartals Hinweis wird im Word-Bit (Bit 15) mit einem Nullwert (0) angegeben.</span><span class="sxs-lookup"><span data-stu-id="88c00-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="88c00-122">Der Rest des Worts enthält den Hinweis Ticks pro Quartal.</span><span class="sxs-lookup"><span data-stu-id="88c00-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="88c00-123">Ein mit einem Stream von MIDI-Daten verknüpfter Wert wird in Einheiten (Mikrosekunden pro Quartals Notiz) gespeichert, die mit der *Standard mäßigen-Standard-Datei 1,0* -Spezifikation übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="88c00-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="88c00-124">Beispiel: ein Quartals Hinweis in 4/4-Zeit, der ein Tempo von 500.000 Mikrosekunden pro Quartals Notiz verwendet, wird mit der Rate von 120 Beats pro Minute abgespielt.</span><span class="sxs-lookup"><span data-stu-id="88c00-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="88c00-125">SMPTE-Zeit Abteilungs Formate geben die Länge eines Takts vollständig an, ohne dass die Notwendigkeit von Tempo Informationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="88c00-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="88c00-126">Bei Verwendung von SMPTE-Zeitformaten können MIDI-Sequenzen mit anderen SMPTE-Ereignissen synchronisiert werden, z. b. Video-oder stripesetaudiodaten.</span><span class="sxs-lookup"><span data-stu-id="88c00-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="88c00-127">Die SMPTE-Zeit wird mit einem Wert von 1 im höherwertigen Bit (Bit 15) des Zeit Teilungs Worts angegeben.</span><span class="sxs-lookup"><span data-stu-id="88c00-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="88c00-128">Der Rest des signifikantesten Bytes gibt das verwendete SMPTE-Format als negative Werte an.</span><span class="sxs-lookup"><span data-stu-id="88c00-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="88c00-129">Die unterstützten SMPTE-Formate und ihre entsprechenden Werte (in Klammern) sind 24 (-24), 25 (-25), 30 (-30) und 30 Drop (-29).</span><span class="sxs-lookup"><span data-stu-id="88c00-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="88c00-130">Das niedrige Byte des Zeit Teilungs Worts gibt die Anzahl der Ticks pro SMPTE-Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="88c00-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 