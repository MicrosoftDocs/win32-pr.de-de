---
title: Suchen in ASF-Dateien (Windows Media Format 11 SDK)
description: Suchen in ASF-Dateien
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media-Format-SDK, suchen in ASF-Dateien
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), suchen
- ASF (Advanced Systems Format), suchen
- DirectShow, suchen in ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039933"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="292e3-110">Suchen in ASF-Dateien (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="292e3-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="292e3-111">Der [WM-ASF-Reader](wm-asf-reader-filter.md)kann über seine **imediaseeking** -Schnittstelle eine sehr genaue Temporale Suche auf Windows Media – basierten Inhalten mit einem temporalen Index durchführen.</span><span class="sxs-lookup"><span data-stu-id="292e3-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="292e3-112">(Alle Frame indizierten Inhalte enthalten auch einen temporalen Index.) Garantierte Frame-exakte Suchvorgänge werden im WM-ASF-Reader nicht direkt unterstützt. es gibt jedoch eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="292e3-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="292e3-113">Verwenden Sie zunächst das Windows Media-Format-SDK direkt zum Erstellen einer Instanz des synchronen Reader-Objekts, öffnen Sie die Datei, rufen Sie den einem angegebenen Frame zugeordneten Zeitstempel ab, und verwenden Sie dann die Schnittstelle DirectShow **imediaseeking** , um zu diesem Zeitpunkt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="292e3-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="292e3-114">Die DirectShow **ivideoframestep** -Schnittstelle unterstützt keine Frame genaue Suche von Windows Media – basierten Inhalten.</span><span class="sxs-lookup"><span data-stu-id="292e3-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="292e3-115">Das dsseekfm-Beispiel im Windows Media-Format-SDK veranschaulicht, wie Sie eine Frame genaue Suche mithilfe des WM-ASF-Readers durchführen können.</span><span class="sxs-lookup"><span data-stu-id="292e3-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="292e3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="292e3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="292e3-117">**WM-ASF-Lesefilter**</span><span class="sxs-lookup"><span data-stu-id="292e3-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




