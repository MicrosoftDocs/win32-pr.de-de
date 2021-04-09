---
title: So erhalten Sie Leistungsstatistiken für Leser
description: So erhalten Sie Leistungsstatistiken für Leser
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), Reader-Leistungsstatistik
- ASF (Advanced Systems Format), Reader-Leistungsstatistik
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Leistungsstatistik
- ASF (Advanced Systems Format), Leistungsstatistik
- asynchrone Leser, Leistungsstatistiken
- Leistung, Leser Statistik
- Leistung, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858003"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="09604-112">So erhalten Sie Leistungsstatistiken für Leser</span><span class="sxs-lookup"><span data-stu-id="09604-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="09604-113">Wenn Dateien lokal mit dem asynchronen Reader gelesen werden, ist es nicht erforderlich, die Leistung von Lesevorgängen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="09604-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="09604-114">Wenn Ihre Anwendung jedoch aus einer Streamingquelle liest, kann die Leistungsstatistik sehr wichtig sein.</span><span class="sxs-lookup"><span data-stu-id="09604-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="09604-115">Ihre Anwendung kann auf Änderungen der Wiedergabe Leistung reagieren, um die bestmögliche Endbenutzer Leistung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="09604-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="09604-116">Die Leistungsinformationen, die Sie aus dem Reader abrufen können, umfassen die folgenden Statistiken:</span><span class="sxs-lookup"><span data-stu-id="09604-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="09604-117">Die aktuelle Bandbreite der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="09604-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="09604-118">Die Anzahl der vom Server empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="09604-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="09604-119">Die Anzahl verlorener Pakete, die wieder hergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="09604-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="09604-120">Die Anzahl verlorener Pakete, die nicht wieder hergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="09604-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="09604-121">Der Prozentsatz der empfangenen Gesamtzahl der gesendeten Pakete.</span><span class="sxs-lookup"><span data-stu-id="09604-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="09604-122">Führen Sie die folgenden Schritte aus, um Leistungsstatistiken für Leser zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="09604-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="09604-123">Erstellen Sie vor der Wiedergabe eine Statistik für die [**WM-Reader- \_ \_ Statistik**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="09604-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="09604-124">Sie müssen das **CBSIZE** -Member auf sizeof (WM \_ Reader \_ Statistics) festlegen.</span><span class="sxs-lookup"><span data-stu-id="09604-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="09604-125">Abrufen eines Zeigers auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="09604-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="09604-126">Führen Sie während der Wiedergabe häufig Aufrufe von [**iwmreaderadvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) aus, um die Leistung zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="09604-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="09604-127">Übergeben Sie Ihre **WM- \_ Reader- \_ Statistik** Struktur mit jedem-Befehl, und untersuchen Sie die entsprechenden Member.</span><span class="sxs-lookup"><span data-stu-id="09604-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09604-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09604-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09604-129">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="09604-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




