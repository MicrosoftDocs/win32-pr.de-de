---
title: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe
description: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- Wellenform-Audiodatei, Verwalten der Wiedergabe mit Meldungen
- Waveform-Audioschnittstelle, Verwalten der Wiedergabe mit Nachrichten
- Wiedergabe von Waveform-Audiodateien, Verwalten der Wiedergabe mit Nachrichten
- Wellenform-Audiodaten, Meldungen
- Waveform-Audioschnittstelle, Meldungen
- Wiedergabe von Waveform-Audiodateien, Nachrichten
- MM_WOM_CLOSE Meldung
- MM_WOM_DONE Meldung
- MM_WOM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314853"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="d1a33-112">Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d1a33-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="d1a33-113">Die folgenden Meldungen können an eine Fenster Prozedur Funktion zum Verwalten der Waveform-Audiowiedergabe gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1a33-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="d1a33-114">`Message`</span><span class="sxs-lookup"><span data-stu-id="d1a33-114">Message</span></span>                                | <span data-ttu-id="d1a33-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1a33-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a33-116">**MM \_ WOM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="d1a33-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="d1a33-117">Wird gesendet, wenn das Gerät mit der [**waveoutclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) -Funktion geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d1a33-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="d1a33-118">**MM \_ WOM \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="d1a33-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="d1a33-119">Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mithilfe der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1a33-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="d1a33-120">**MM \_ WOM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="d1a33-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="d1a33-121">Wird gesendet, wenn das Gerät mithilfe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d1a33-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="d1a33-122">Jedem dieser Nachrichten ist ein *wParam* -Parameter und ein *LPARAM* -Parameter zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d1a33-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="d1a33-123">Der *wParam* -Parameter gibt immer ein Handle des geöffneten Waveform-Audiogeräts an.</span><span class="sxs-lookup"><span data-stu-id="d1a33-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="d1a33-124">Bei der Meldung [**mm \_ WOM \_ done**](mm-wom-done.md) gibt *LPARAM* einen Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur an, die den abgeschlossenen Datenblock identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d1a33-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="d1a33-125">Der *LPARAM* -Parameter wird nicht für die geöffneten Meldungen [**mm \_ WOM \_ Close**](mm-wom-close.md) und [**mm \_ WOM \_**](mm-wom-open.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1a33-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="d1a33-126">Die nützlichste Meldung ist wahrscheinlich mm \_ WOM \_ .</span><span class="sxs-lookup"><span data-stu-id="d1a33-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="d1a33-127">Wenn diese Meldung signalisiert, dass die Wiedergabe eines Datenblocks beendet ist, können Sie den Datenblock bereinigen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="d1a33-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="d1a33-128">Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, müssen Sie die \_ Nachrichten von mm WOM \_ Öffnen und mm \_ WOM \_ Schließen wahrscheinlich nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d1a33-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="d1a33-129">Die Rückruffunktion für Waveform-Audioausgabegeräte wird von der Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d1a33-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="d1a33-130">Weitere Informationen zu dieser Rückruffunktion finden Sie unter der [**waveoutproc**](/previous-versions//dd743869(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d1a33-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 