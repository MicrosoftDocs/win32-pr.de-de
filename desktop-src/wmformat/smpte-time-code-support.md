---
title: SMPTE-Zeit Code Unterstützung
description: SMPTE-Zeit Code Unterstützung
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- Windows Media-Format-SDK, iwmreadertimecode-Schnittstelle
- Advanced Systems Format (ASF), iwmreadertimecode-Schnittstelle
- ASF (Advanced Systems Format), iwmreadertimecode-Schnittstelle
- SMPTE-Zeit Codes, Informationen zu
- Iwmreadertimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516610"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="b80e9-111">SMPTE-Zeit Code Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b80e9-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="b80e9-112">Das Windows Media-Format SDK bietet eingeschränkte Unterstützung für SMPTE-Zeit Code, d. h. ein Standardmäßiges Zeit Code Format für Filme und Fernsehen.</span><span class="sxs-lookup"><span data-stu-id="b80e9-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="b80e9-113">Sie können SMPTE-Zeit Code Daten mit Beispielen als Erweiterungen für Dateneinheiten einschließen.</span><span class="sxs-lookup"><span data-stu-id="b80e9-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="b80e9-114">Der Datenteil der Erweiterung ist eine [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Struktur, die die Informationen aus dem ursprünglichen SMPTE-Zeitstempel enthält.</span><span class="sxs-lookup"><span data-stu-id="b80e9-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="b80e9-115">Die Wartung von SMPTE-Zeit Code in ihren ASF-Dateien umfasst Leistungs Limits.</span><span class="sxs-lookup"><span data-stu-id="b80e9-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="b80e9-116">Jede Stichprobe mit einem zugeordneten SMPTE-Zeitstempel erfordert den Transport der 14 Bytes in der Zeitstempel Struktur.</span><span class="sxs-lookup"><span data-stu-id="b80e9-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="b80e9-117">In einem Streamingszenario könnte diese größere Bandbreiten Anforderung katastrophal sein.</span><span class="sxs-lookup"><span data-stu-id="b80e9-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="b80e9-118">Daher wird empfohlen, dass SMPTE-Zeit Codes bei der Videobearbeitung nur in ASF-Dateien persistent gespeichert werden. Dies erfolgt in der Regel mit lokalen Dateien.</span><span class="sxs-lookup"><span data-stu-id="b80e9-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="b80e9-119">Wenn die endgültige Datei erstellt wurde, sollten Sie die Dateneinheiten Erweiterungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="b80e9-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="b80e9-120">Sie können SMPTE-Zeitstempel so lesen, wie Sie jede andere Erweiterung für Dateneinheiten lesen würden, aber die Lese Objekte bieten integrierte Unterstützung für die Suche nach SMPTE-Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="b80e9-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="b80e9-121">Um nach SMPTE-Zeitstempeln suchen zu können, müssen Sie zunächst die Datei nach SMPTE-Zeit Code indizieren.</span><span class="sxs-lookup"><span data-stu-id="b80e9-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="b80e9-122">Sie können den Indexer so konfigurieren, dass Zeit Codes mithilfe der [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) -Methode indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b80e9-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="b80e9-123">Mithilfe des asynchronen Readers können Sie mithilfe der Methoden der [**iwmreadertimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) -Schnittstelle und der [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) -Methode von SMPTE-Zeitstempeln aus in einer Datei navigieren.</span><span class="sxs-lookup"><span data-stu-id="b80e9-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="b80e9-124">Verwenden Sie [**IWMSyncReader2:: setrangebytimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode)mit dem synchronen Reader.</span><span class="sxs-lookup"><span data-stu-id="b80e9-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b80e9-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b80e9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b80e9-126">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="b80e9-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="b80e9-127">**Konfigurieren von Dateneinheitserweiterung en**</span><span class="sxs-lookup"><span data-stu-id="b80e9-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




