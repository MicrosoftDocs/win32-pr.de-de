---
description: Suchen in ASF-Dateien
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Suchen in ASF-Dateien (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521288"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="a1590-103">Suchen in ASF-Dateien (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="a1590-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="a1590-104">Der [WM-ASF-Reader](wm-asf-reader-filter.md)kann über seine [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle eine sehr genaue Temporale Suche auf Windows Media – basierten Inhalten mit einem temporalen Index durchführen.</span><span class="sxs-lookup"><span data-stu-id="a1590-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="a1590-105">(Alle Frame indizierten Inhalte enthalten auch einen temporalen Index.) Garantierte Frame-exakte Suchvorgänge werden im WM-ASF-Reader nicht direkt unterstützt. es gibt jedoch eine Möglichkeit, dies zu tun, wenn Sie diese Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="a1590-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="a1590-106">Verwenden Sie zunächst das Windows Media-Format-SDK direkt zum Erstellen einer Instanz des synchronen Reader-Objekts, öffnen Sie die Datei, rufen Sie den einem angegebenen Frame zugeordneten Zeitstempel ab, und verwenden Sie dann die Schnittstelle DirectShow **imediaseeking** , um zu diesem Zeitpunkt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a1590-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="a1590-107">Die [**ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) -Schnittstelle unterstützt keine Frame genaue Suche von Windows Media – basierten Inhalten.</span><span class="sxs-lookup"><span data-stu-id="a1590-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1590-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1590-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1590-109">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1590-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



