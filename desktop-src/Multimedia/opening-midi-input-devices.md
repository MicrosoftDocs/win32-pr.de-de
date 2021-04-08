---
title: Öffnen von MIDI-Eingabegeräten
description: Öffnen von MIDI-Eingabegeräten
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabegeräte
- MIDI (Digital Instrumentation Digital Interface), Eingabegeräte
- Aufzeichnen von MIDI-Audiodaten, Eingabegeräte
- MIDI-Eingabegeräte
- Digital Instrumentation Digital Interface (MIDI), Öffnen von Eingabegeräten
- MIDI (Digital Instrumentation Digital Interface), Öffnen von Eingabegeräten
- Aufzeichnen von MIDI-Audiodaten, Öffnen von Eingabegeräten
- Öffnen von MIDI-Eingabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726320"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="ac39c-111">Öffnen von MIDI-Eingabegeräten</span><span class="sxs-lookup"><span data-stu-id="ac39c-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="ac39c-112">Verwenden Sie zum Öffnen eines MIDI-Eingabe Geräts für die Aufzeichnung die [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ac39c-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="ac39c-113">Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle an einen angegebenen Speicherort geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ac39c-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="ac39c-114">Wenn Sie das Integritäts Kennzeichen für das MIDI-e/a \_ \_ mit **midiinopen** verwenden, verwendet das System die [**MIM \_ MoreData**](mim-moredata.md) -Nachricht, um die Rückruffunktion Ihrer Anwendung zu benachrichtigen, wenn die Daten von MIDI nicht schnell genug verarbeitet werden, um mit dem Eingabegeräte Treiber Schritt zu halten.</span><span class="sxs-lookup"><span data-stu-id="ac39c-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="ac39c-115">(Die [**mm \_ MIM \_ MoreData**](mm-mim-moredata.md) -Nachricht führt den gleichen Auftrag mit Fenster Rückrufen aus.</span><span class="sxs-lookup"><span data-stu-id="ac39c-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="ac39c-116">Aus Leistungsgründen werden von den meisten Anwendungen jedoch Rückruf Funktionen anstelle von Fenster Rückrufen verwendet.) Wenn Ihre Anwendung die Daten von MIDI in einem separaten Thread verarbeitet, kann sich die Erhöhung der Thread Priorität erheblich auf die Fähigkeit der Anwendung auswirken, mit dem Datenfluss Schritt zu halten.</span><span class="sxs-lookup"><span data-stu-id="ac39c-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac39c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac39c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac39c-118">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="ac39c-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 