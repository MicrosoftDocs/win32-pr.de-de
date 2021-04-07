---
title: Senden von MIDI-Nachrichten mit streampuffern
description: Senden von MIDI-Nachrichten mit streampuffern
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Abspielen von MIDI-Dateien, Streampuffer
- Streampuffer, Senden von MIDI-Nachrichten
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725360"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="f354c-111">Senden von MIDI-Nachrichten mit streampuffern</span><span class="sxs-lookup"><span data-stu-id="f354c-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="f354c-112">Wenn Ihre Anwendung mit streampuffern arbeitet, wird die [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) -Funktion verwendet, um alle (kurzen und langen) MIDI-Nachrichten an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="f354c-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="f354c-113">Um streamdatenblöcke anzugeben, verwenden Sie die [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -und [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f354c-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="f354c-114">Die **midihdr** -Struktur enthält die Adresse eines gesperrten Datenblocks, die datenblocklänge und einige sortierte Flags.</span><span class="sxs-lookup"><span data-stu-id="f354c-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="f354c-115">Die Daten werden in Form von **MidiEvent** -Strukturen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f354c-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="f354c-116">Das System erzwingt eine Größenbeschränkung von 64 KB für Streampuffer.</span><span class="sxs-lookup"><span data-stu-id="f354c-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="f354c-117">Nachdem Sie **mithilfe von midistreamout** einen Streampuffer mit Daten gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="f354c-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="f354c-118">Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss der einzelnen Datenblöcke überwachen, damit Sie wissen, wann zusätzliche Blöcke gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f354c-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="f354c-119">Informationen zu den verschiedenen Techniken zum Überwachen der Datenblock Vervollständigung finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="f354c-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 