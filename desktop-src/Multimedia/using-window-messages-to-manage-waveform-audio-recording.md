---
title: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung
description: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- Wellenform-Audiodatei, Verwalten der Aufzeichnung mit Nachrichten
- Waveform-Audioschnittstelle, Verwalten der Aufzeichnung mit Nachrichten
- Aufzeichnen von Wellenform-Audiodaten, Verwalten der Aufzeichnung mit Nachrichten
- Wellenform-Audiodaten, Meldungen
- Waveform-Audioschnittstelle, Meldungen
- Aufzeichnen von Wellenform-Audiodaten, Nachrichten
- MM_WIM_CLOSE Meldung
- MM_WIM_DATA Meldung
- MM_WIM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472836"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="6dfbf-112">Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6dfbf-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="6dfbf-113">Die folgenden Meldungen können an eine Fenster Prozedur Funktion zum Verwalten der Waveform-Audioaufzeichnung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="6dfbf-114">`Message`</span><span class="sxs-lookup"><span data-stu-id="6dfbf-114">Message</span></span>                                | <span data-ttu-id="6dfbf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dfbf-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dfbf-116">**MM \_ WIM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="6dfbf-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="6dfbf-117">Wird gesendet, wenn das Gerät mithilfe der [**waveinclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="6dfbf-118">**MM- \_ WIM- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="6dfbf-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="6dfbf-119">Wird gesendet, wenn der Gerätetreiber mit einem Puffer fertig ist, der mithilfe der [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) -Funktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="6dfbf-120">**MM \_ WIM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="6dfbf-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="6dfbf-121">Wird gesendet, wenn das Gerät mithilfe der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="6dfbf-122">Der *LPARAM* -Parameter der [**mm-WIM- \_ \_ Daten**](mm-wim-data.md) gibt einen Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur an, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="6dfbf-123">Dieser Puffer ist möglicherweise nicht vollständig mit Waveform-Audiodaten gefüllt. Aufzeichnung kann angehalten werden, bevor der Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="6dfbf-124">Verwenden Sie den **dwbytesrecorded** -Member der **wavehdr** -Struktur, um die Menge der gültigen Daten zu ermitteln, die im Puffer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="6dfbf-125">Die nützlichste Meldung ist wahrscheinlich [**mm \_ WIM- \_ Daten**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="6dfbf-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="6dfbf-126">Wenn die Anwendung mit dem vom Gerätetreiber gesendeten Datenblock abgeschlossen ist, können Sie den Datenblock bereinigen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="6dfbf-127">Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, müssen Sie die mm-WIM-Nachrichten ( [**\_ WIM \_ Open**](mm-wim-open.md) und [**mm \_ \_**](mm-wim-close.md) ) wahrscheinlich nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="6dfbf-128">Die Rückruffunktion für Waveform-Audioeingabegeräte wird von der Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="6dfbf-129">Weitere Informationen zu dieser Rückruffunktion finden Sie unter der [**waveinproc**](/previous-versions//dd743849(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6dfbf-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dfbf-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dfbf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dfbf-131">Aufzeichnen von Waveform-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="6dfbf-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 