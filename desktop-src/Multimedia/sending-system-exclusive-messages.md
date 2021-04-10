---
title: Senden von System-Exclusive Nachrichten
description: Senden von System-Exclusive Nachrichten
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), System exklusive Meldungen
- MIDI (Digital Instrumentation Digital Interface), System exklusive Nachrichten
- Abspielen von MIDI-Dateien, System exklusive Nachrichten
- System exklusive MIDI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858167"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="0e382-111">Senden von System-Exclusive Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0e382-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="0e382-112">System exklusive System-Nachrichten sind die einzigen MIDI-Nachrichten, die nicht in einen einzelnen Double Word-Wert passen.</span><span class="sxs-lookup"><span data-stu-id="0e382-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="0e382-113">System exklusive Nachrichten können eine beliebige Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e382-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="0e382-114">Windows stellt die [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) -Funktion zum Senden von System exklusiven Nachrichten an die MIDI-Ausgabegeräte bereit.</span><span class="sxs-lookup"><span data-stu-id="0e382-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="0e382-115">Verwenden Sie die [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, um System exklusive Systemdaten Blöcke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e382-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="0e382-116">Nachdem Sie einen System exklusiven Datenblock mithilfe von **midioutlongmsg** gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="0e382-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="0e382-117">Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss der einzelnen Datenblöcke überwachen, damit Sie wissen, wann zusätzliche Blöcke gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e382-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="0e382-118">Informationen zu den verschiedenen Techniken zum Überwachen der Datenblock Vervollständigung finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="0e382-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="0e382-119">Alle anderen Bytes als eine System-Real-Time-Nachricht beenden eine System exklusive Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0e382-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="0e382-120">Wenn Sie mehrere Datenblöcke verwenden, um eine einzelne System exklusive Nachricht zu senden, senden Sie keine anderen als System-Real-Time-Meldungen zwischen den Datenblöcken.</span><span class="sxs-lookup"><span data-stu-id="0e382-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 