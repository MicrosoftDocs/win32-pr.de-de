---
title: Anfordern von Zeitformaten
description: Anfordern von Zeitformaten
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Digital Instrumentation Digital Interface (MIDI), Zeitformate
- MIDI (Digital Interface Digital Interface), Zeitformate
- MIDI-Dienste, Zeitformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724808"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="36270-106">Anfordern von Zeitformaten</span><span class="sxs-lookup"><span data-stu-id="36270-106">Requesting Time Formats</span></span>

<span data-ttu-id="36270-107">Windows verwendet die [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur, um die Zeit in einem oder mehreren unterschiedlichen Formaten darzustellen, einschließlich der Millisekunden, Samples, SMPTE und der Formatvorlagen-Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="36270-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="36270-108">Der **wType** -Member gibt das Zeitformat an.</span><span class="sxs-lookup"><span data-stu-id="36270-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="36270-109">Die [**midistreamposition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) -Funktion verwendet die **mmtime** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="36270-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="36270-110">Bevor Sie diese Funktion aufrufen, müssen Sie das **wType** -Element festlegen, um das angeforderte Zeitformat anzugeben.</span><span class="sxs-lookup"><span data-stu-id="36270-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="36270-111">Um festzustellen, ob das angeforderte Zeitformat unterstützt wird, überprüfen Sie **wType** nach dem Aufruf.</span><span class="sxs-lookup"><span data-stu-id="36270-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="36270-112">Wenn das angeforderte Zeitformat nicht unterstützt wird, wird die Uhrzeit in einem vom Gerätetreiber ausgewählten Alternativen Zeitformat angegeben, und das **wType** -Element wird so geändert, dass das ausgewählte Zeitformat angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="36270-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="36270-113">Weitere Informationen zur **mmtime** -Struktur finden Sie unter [Multimedia-Timer](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="36270-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36270-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36270-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36270-115">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="36270-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 