---
title: So erhalten Sie eine Writer-Statistik
description: So erhalten Sie eine Writer-Statistik
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), Writer Statistics
- ASF (Advanced Systems Format), Writer Statistics
- Writer-Statistik, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948510"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="e0db8-106">So erhalten Sie eine Writer-Statistik</span><span class="sxs-lookup"><span data-stu-id="e0db8-106">To Get Writer Statistics</span></span>

<span data-ttu-id="e0db8-107">Der Writer kann statistische Informationen zu Schreibvorgängen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e0db8-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="e0db8-108">Es gibt zwei Methoden zum Sammeln von Writer-Statistiken: [**iwmbeschreiteradvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) und [**IWMWriterAdvanced3:: getstatisticsex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="e0db8-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="e0db8-109">Die von **getstatisticsex** abgerufenen Informationen sind spezifischer als die von **getstatistics** abgerufenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="e0db8-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="e0db8-110">Beide Methoden füllen Strukturen mit statistischen Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="e0db8-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="e0db8-111">**Getstatistics** verwendet die [**WM \_ Writer \_ Statistics**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) -Struktur, und **getstatisticsex** verwendet die " [**WM \_ Writer \_ Statistics \_ Ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="e0db8-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="e0db8-112">" **Getstatisticsex** " dupliziert die von " **getstatistics**" erhaltenen Daten nicht.</span><span class="sxs-lookup"><span data-stu-id="e0db8-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="e0db8-113">Um möglichst umfassende Informationen zu erhalten, sollten Sie beide Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e0db8-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0db8-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0db8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0db8-115">**Iwmschreiteradvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e0db8-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="e0db8-116">**IWMWriterAdvanced3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e0db8-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="e0db8-117">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="e0db8-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




