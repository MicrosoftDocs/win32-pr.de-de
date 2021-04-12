---
title: Öffnen von MIDI-Ausgabegeräten
description: Öffnen von MIDI-Ausgabegeräten
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte
- MIDI (Digital Instrumentation Digital Interface), Ausgabegeräte
- Abspielen von MIDI-Dateien, Ausgabe von Geräten
- MIDI-Ausgabegeräte
- Digital Instrumentation Digital Interface (MIDI), Öffnen von Ausgabegeräten
- MIDI (Digital Instrumentation Digital Interface), Öffnen von Ausgabegeräten
- Abspielen von MIDI-Dateien, Öffnen von Ausgabegeräten
- Öffnen von MIDI-Ausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472964"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="dd283-111">Öffnen von MIDI-Ausgabegeräten</span><span class="sxs-lookup"><span data-stu-id="dd283-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="dd283-112">Verwenden Sie die [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion, um ein-Ausgabegerät für die Wiedergabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd283-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="dd283-113">Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle an einen angegebenen Speicherort geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dd283-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="dd283-114">Einer der Parameter von **midioutopen** ist ein Double Word-Wert.</span><span class="sxs-lookup"><span data-stu-id="dd283-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="dd283-115">Dieser Wert gibt ein Fenster oder Thread handle, ein Ereignis handle oder die Adresse einer Rückruffunktion an, die verwendet wird, um den Fortschritt der Wiedergabe von System exklusiven System exklusiven Daten und streampuffern zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="dd283-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="dd283-116">Mithilfe der Überwachung kann die Anwendung bestimmen, wann zusätzliche Datenblöcke gesendet werden sollen und wann Datenblöcke freigegeben werden sollen, die gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="dd283-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="dd283-117">Weitere Informationen zu diesen Methoden finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="dd283-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 