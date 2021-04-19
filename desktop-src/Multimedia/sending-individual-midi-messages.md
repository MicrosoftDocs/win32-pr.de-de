---
title: Senden einzelner MIDI-Nachrichten
description: Senden einzelner MIDI-Nachrichten
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), individuelle Nachrichten
- MIDI (Digital Instrumentation Digital Interface), individuelle Nachrichten
- Abspielen von MIDI-Dateien, einzelnen Nachrichten
- einzelne MIDI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339875"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="e6ca2-111">Senden einzelner MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e6ca2-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="e6ca2-112">Sie können mit den folgenden Funktionen mit einzelnen MIDI-Nachrichten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="e6ca2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ca2-113">Value</span></span>                                      | <span data-ttu-id="e6ca2-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e6ca2-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6ca2-115">**midioutlongmsg**</span><span class="sxs-lookup"><span data-stu-id="e6ca2-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="e6ca2-116">Sendet einen Puffer von MIDI-Daten an das angegebene MIDI-Ausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="e6ca2-117">Verwenden Sie diese Funktion, um System exklusive Nachrichten an ein MIDI-Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="e6ca2-118">**falsch einwählsatz**</span><span class="sxs-lookup"><span data-stu-id="e6ca2-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="e6ca2-119">Deaktiviert alle Notizen für ein angegebenes MIDI-Ausgabegerät in allen Kanälen.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="e6ca2-120">Alle ausstehenden System exklusiven Puffer und Streampuffer werden als abgeschlossen markiert und an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="e6ca2-121">**midioutshortmsg**</span><span class="sxs-lookup"><span data-stu-id="e6ca2-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="e6ca2-122">Sendet eine MIDI-Nachricht an ein angegebenes MIDI-Ausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="e6ca2-123">Verwenden Sie [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg), um eine beliebige MIDI-Nachricht (mit Ausnahme von System exklusiven Nachrichten) zu senden.</span><span class="sxs-lookup"><span data-stu-id="e6ca2-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 