---
title: Zurücksetzen der MIDI-Ausgabe
description: Zurücksetzen der MIDI-Ausgabe
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte zurücksetzen
- MIDI (Digital Instrumentation Digital Interface), Zurücksetzen von Ausgabegeräten
- Abspielen von MIDI-Dateien, Zurücksetzen von Ausgabegeräten
- Zurücksetzen von Ausgabegeräten
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte
- MIDI (Digital Instrumentation Digital Interface), Ausgabegeräte
- Abspielen von MIDI-Dateien, Ausgabe von Geräten
- MIDI-Ausgabegeräte
- EOX (Ende der exklusiven)
- Ende der exklusiven (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314685"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="33ea3-113">Zurücksetzen der MIDI-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="33ea3-113">Resetting MIDI Output</span></span>

<span data-ttu-id="33ea3-114">Die [**midiversiset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) -Funktion deaktiviert alle Notizen für alle MIDI-Kanäle für ein bestimmtes MIDI-Gerät.</span><span class="sxs-lookup"><span data-stu-id="33ea3-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="33ea3-115">Anschließend werden alle ausstehenden System exklusiven Puffer als abgeschlossen markiert und an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="33ea3-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="33ea3-116">Diese Funktion kann in einer Anwendung nützlich sein, die die Verwendung von MIDI verwendet, um dem Benutzer die Möglichkeit zu geben, die MIDI-Ausgabe zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="33ea3-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="33ea3-117">Das Beenden einer System exklusiven Nachricht, ohne ein EOX-Byte zu senden, kann Probleme für das empfangende Gerät verursachen.</span><span class="sxs-lookup"><span data-stu-id="33ea3-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="33ea3-118">Die **midibereichset** -Funktion sendet kein EOX-Byte, wenn Sie eine System exklusive Nachricht beendet, da Anwendungen dafür verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="33ea3-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 