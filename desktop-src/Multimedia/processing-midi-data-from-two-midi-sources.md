---
title: Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen
description: Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows Multimedia, Verarbeiten von MIDI-Daten aus zwei Quellen
- Multimedia, Verarbeiten von MIDI-Daten aus zwei Quellen
- Multimedia-Audiodaten, Verarbeiten von MIDI-Daten aus zwei Quellen
- Audiodaten, Verarbeiten von MIDI-Daten aus zwei Quellen
- Digital Instrumentation Digital Interface (MIDI), Verarbeiten von Daten aus zwei Quellen
- MIDI (Digital Instrumentation Digital Interface), Verarbeiten von Daten aus zwei Quellen
- Verarbeiten von MIDI-Daten aus zwei Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038924"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="847a0-110">Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen</span><span class="sxs-lookup"><span data-stu-id="847a0-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="847a0-111">Das MIDI-Subsystem kann aus zwei Datenquellen aus zwei Datenquellen für die gleichzeitige Wiedergabe an ein einzelnes MIDI-Ausgabegerät weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="847a0-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="847a0-112">Eine Quelle kann z. b. Hintergrundmusik oder eine Bass Linie sein, die vorab aufgezeichnet und in einer Datei gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="847a0-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="847a0-113">Bei der zweiten Quelle kann es sich um Livedaten aus einem MIDI-Instrument wie Tastatur oder Gitarre handeln.</span><span class="sxs-lookup"><span data-stu-id="847a0-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="847a0-114">Beide Datenquellen senden MIDI-Daten an ein einzelnes, mit einem Handle bezeichnetes-Gerät.</span><span class="sxs-lookup"><span data-stu-id="847a0-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="847a0-115">Senden eines Datenstroms mithilfe der Funktion " [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) " und eines oder mehrerer Streampuffer.</span><span class="sxs-lookup"><span data-stu-id="847a0-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="847a0-116">Dieser Datenstream enthält normalerweise vorab Daten, die in den Puffer gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="847a0-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="847a0-117">Senden Sie den zweiten Datenstrom (in der Regel von einem MIDI-Instrument) mithilfe der [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) -Funktion asynchron.</span><span class="sxs-lookup"><span data-stu-id="847a0-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="847a0-118">Der laufende Status eines Streampuffers wird von den asynchronen Aufrufen durch den zweiten Datenstrom nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="847a0-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="847a0-119">Jede mit **midioutshortmsg** gesendete kurze Nachricht muss eine komplette MIDI-Nachricht mit einem Status Byte und der entsprechenden Anzahl von Daten Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="847a0-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="847a0-120">Wenn das Status Byte ausgelassen wird, gibt **midioutshortmsg** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="847a0-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="847a0-121">(Es gibt jedoch keinen ausgegebene Status mit Datenstrom Ausgabe.)</span><span class="sxs-lookup"><span data-stu-id="847a0-121">(However, there is no running status with stream output.)</span></span>

 

 