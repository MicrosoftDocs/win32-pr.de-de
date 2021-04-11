---
title: Angeben von Zeitformaten
description: Angeben von Zeitformaten
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Mciwndgettimeformat-Makro
- Mciwndsettimeformat-Makro
- Mciwnduationtime-Makro
- Mciwnduabframes-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310071"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="e839c-107">Angeben von Zeitformaten</span><span class="sxs-lookup"><span data-stu-id="e839c-107">Specifying Time Formats</span></span>

<span data-ttu-id="e839c-108">Multimediare-Datentypen können in der Regel Zeit verwenden, um signifikante Positionen innerhalb ihrer Inhalte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e839c-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="e839c-109">Allgemeine Zeitformate sind Millisekunden, nachverfolgt und Frames. andere weniger gängige Zeitformate, wie z. b. SMPTE (Society of Motion Picture und TV Engineers) 24, sind ebenfalls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e839c-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="e839c-110">Zeit ist das Format und das Referenzsystem für Waveform-Audiodaten, MIDI und CD-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="e839c-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="e839c-111">Video unterstützt Zeit, obwohl es als Sequenz von Frames (Stream) aufgezeichnet wird, die in der Regel mit einer bestimmten Geschwindigkeit wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e839c-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="e839c-112">Zum Festlegen des Zeit Formats sind mehrere Makros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e839c-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="e839c-113">Sie können das aktuelle Zeitformat für eine Datei oder ein Gerät abrufen, indem Sie das [**mciwndgettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e839c-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="e839c-114">Sie können das aktuelle Zeitformat in ein beliebiges anderes Zeitformat ändern, das von einem Gerät unterstützt wird, indem Sie das [**mciwndsettimeformat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e839c-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="e839c-115">Sie können auch das Zeitformat auf Millisekunden oder Frames festlegen, indem Sie die Makros [**mciwndusetime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) oder [**mciwnduseframes**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e839c-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="e839c-116">Nicht kontinuierliche Formate, wie z. b. "Tracks" und "SMPTE", können dazu führen, dass sich die Symbolleiste im-</span><span class="sxs-lookup"><span data-stu-id="e839c-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="e839c-117">In diesen Zeitformaten können Sie die Symbolleiste ausschalten, indem Sie \_ beim Erstellen eines mciwnd-Fensters den Fenster Stil mciwndf noplaybar angeben.</span><span class="sxs-lookup"><span data-stu-id="e839c-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




