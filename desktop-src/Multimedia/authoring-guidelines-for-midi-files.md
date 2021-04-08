---
title: Erstellungs Richtlinien für MIDI-Dateien
description: Erstellungs Richtlinien für MIDI-Dateien
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Digital Instrumentation Digital Interface (MIDI), Richtlinien zum Erstellen von Dateien
- MIDI (Digital Instrumentation Digital Interface), Richtlinien für die Dateierstellung
- Erstellen von MIDI-Dateien, Richtlinien zum Erstellen von Dateien
- standardmäßige MIDI-patchzuweisungen
- Standard-MIDI-schlüsselzuweisungen
- Digital Instrumentation Digital Interface (MIDI), Standard-patchzuweisungen
- MIDI (Digital Instrumentation Digital Interface), Standard-patchzuweisungen
- Digital Instrumentation Digital Interface (MIDI), Standardschlüssel Zuweisungen
- MIDI (Digital Interface Digital Interface), Standardschlüssel Zuweisungen
- Erstellen von MIDI-Dateien, Standard-patchzuweisungen
- Erstellen von MIDI-Dateien, Standardschlüssel Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037519"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="61068-114">Erstellungs Richtlinien für MIDI-Dateien</span><span class="sxs-lookup"><span data-stu-id="61068-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="61068-115">Befolgen Sie diese Richtlinien, um geräteunabhängige MIDI-Dateien für Windows zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="61068-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="61068-116">Verwenden Sie die [standardmäßigen MIDI-patchzuweisungen](standard-midi-patch-assignments.md) und die [Standard-MIDI-schlüsselzuweisungen](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="61068-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="61068-117">Senden Sie immer eine Programm Änderungs Meldung an einen Kanal, um einen Patch auszuwählen, bevor andere Nachrichten an diesen Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="61068-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="61068-118">Wählen Sie für die beiden Percussion-Kanäle (10 und 16) Programmnummer 0 aus.</span><span class="sxs-lookup"><span data-stu-id="61068-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="61068-119">Befolgen Sie immer eine Nachricht vom Typ "MIDI-Programm ändern" mit einer Nachricht vom Typ "MIDI Main-Volume Controller" (Controller Nummer 7), um das relative Volume des Patches festzulegen.</span><span class="sxs-lookup"><span data-stu-id="61068-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="61068-120">Verwenden Sie für den Haupt volumecontroller den Wert 80 (0x50) für die normalen Empfangs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="61068-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="61068-121">Bei ruhigeren oder lauter Ebenen können Sie niedrigere oder höhere Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="61068-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="61068-122">Verwenden Sie nur die folgenden MIDI-Meldungen: Note-on mit Velocity, Note-Off, Programmänderung, Pitch-Kurve, Haupt Volume (Controller 7) und Dämpferpedal (Controller 64).</span><span class="sxs-lookup"><span data-stu-id="61068-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="61068-123">Interne Synthesizer sind erforderlich, um auf diese Nachrichten zu reagieren, und die meisten von den meisten der von Ihnen darauf antworten.</span><span class="sxs-lookup"><span data-stu-id="61068-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 




