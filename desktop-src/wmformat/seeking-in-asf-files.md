---
title: Suchen in ASF-Dateien (Windows Media Format 11 SDK)
description: Erfahren Sie, wie der WM ASF-Reader eine sehr genaue temporale Suche auf Windows Media-basierten Inhalten durchführen kann, die über einen temporalen Index im Windows Media Format 11 SDK verfügt.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, Suchen in ASF-Dateien
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF),seeking
- ASF (Advanced Systems Format), seeking
- DirectShow,Suchen in ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409883"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="4c032-110">Suchen in ASF-Dateien (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="4c032-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4c032-111">Der [WM ASF-Reader](wm-asf-reader-filter.md)kann über seine **IMediaSeeking-Schnittstelle** sehr genaue temporale Suchmaßnahmen für Windows Media-basierte Inhalte ausführen, die über einen temporalen Index verfügt.</span><span class="sxs-lookup"><span data-stu-id="4c032-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="4c032-112">(Alle frameindizierten Inhalte enthalten auch einen temporalen Index.) Garantierte framegenaue Suchfunktionen werden im WM ASF-Reader nicht direkt unterstützt, aber es gibt eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="4c032-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="4c032-113">Verwenden Sie zunächst das Windows Media Format SDK direkt, um eine Instanz des synchronen Readerobjekts zu erstellen, die Datei zu öffnen, den einem angegebenen Frame zugeordneten Zeitstempel zu erhalten und dann die DirectShow **IMediaSeeking-Schnittstelle** zu verwenden, um nach dieser Zeit zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4c032-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="4c032-114">Die **IVideoFrameStep-Schnittstelle** von DirectShow unterstützt keine framegenaue Suche nach Windows Media-basierten Inhalten.</span><span class="sxs-lookup"><span data-stu-id="4c032-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="4c032-115">Das DSSeekFm-Beispiel im Windows Media Format SDK veranschaulicht, wie Frame-genaue Suchungen mithilfe des WM ASF-Readers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c032-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c032-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c032-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c032-117">**WM ASF-Readerfilter**</span><span class="sxs-lookup"><span data-stu-id="4c032-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




