---
description: Erfahren Sie, wie der WM ASF-Reader eine sehr genaue temporale Suche auf Windows Media-basierten Inhalten durchführen kann, die über einen temporalen Index in DirectShow verfügt.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Suchen in ASF-Dateien (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405583"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="750b9-103">Suchen in ASF-Dateien (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="750b9-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="750b9-104">Der [WM ASF-Reader](wm-asf-reader-filter.md)kann über seine [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) sehr genaue temporale Suchmaßnahmen für Windows Media-basierte Inhalte ausführen, die einen temporalen Index haben.</span><span class="sxs-lookup"><span data-stu-id="750b9-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="750b9-105">(Alle frameindizierten Inhalte enthalten auch einen temporalen Index.) Garantierte framegenaue Suchfunktionen werden im WM ASF-Reader nicht direkt unterstützt, aber es gibt eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="750b9-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="750b9-106">Verwenden Sie zunächst das Windows Media Format SDK direkt, um eine Instanz des synchronen Readerobjekts zu erstellen, die Datei zu öffnen, den einem angegebenen Frame zugeordneten Zeitstempel zu erhalten und dann die DirectShow **IMediaSeeking-Schnittstelle** zu verwenden, um nach dieser Zeit zu suchen.</span><span class="sxs-lookup"><span data-stu-id="750b9-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="750b9-107">Die [**IVideoFrameStep-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) unterstützt keine framegenaue Suche nach Windows Media-basierten Inhalten.</span><span class="sxs-lookup"><span data-stu-id="750b9-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="750b9-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="750b9-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="750b9-109">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="750b9-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



