---
title: DirectShow-qasf-Referenz
description: DirectShow-qasf-Referenz
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media-Format-SDK, qasf
- Windows Media-Format-SDK, DirectShow
- DirectShow, qasf-Referenz
- Qasf-Filter, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390636"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="86ea3-107">DirectShow-qasf-Referenz</span><span class="sxs-lookup"><span data-stu-id="86ea3-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="86ea3-108">Dieser Abschnitt enthält Programmier Verweise für die folgenden DirectShow-qasf-Filter,-Schnittstellen und-Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="86ea3-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="86ea3-109">Die DirectShow-SDK-Dokumentation enthält Referenz-und Programmier Leit Faden Materialien für zusätzliche generische Schnittstellen, die von diesen Filtern verfügbar gemacht werden, wie z. b. **ibasefilter** und **IPin**, sowie für frühere Versionen der qasf-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="86ea3-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="86ea3-110">Eine Erläuterung des qasf-namens finden Sie unter [Informationen zu DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="86ea3-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="86ea3-111">Die folgenden Filter sind in den DirectShow-qasf-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="86ea3-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="86ea3-112">Filtern</span><span class="sxs-lookup"><span data-stu-id="86ea3-112">Filter</span></span>                                           | <span data-ttu-id="86ea3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86ea3-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="86ea3-114">WM-ASF-Lesefilter</span><span class="sxs-lookup"><span data-stu-id="86ea3-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="86ea3-115">Liest und analysiert lokale oder Remote-ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="86ea3-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="86ea3-116">WM-ASF-Writer-Filter</span><span class="sxs-lookup"><span data-stu-id="86ea3-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="86ea3-117">Erstellt ASF-Dateien aus komprimierten oder nicht komprimierten Eingabedaten strömen.</span><span class="sxs-lookup"><span data-stu-id="86ea3-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="86ea3-118">Die folgenden Schnittstellen werden für die Verwendung mit den DirectShow-qasf-Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="86ea3-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="86ea3-119">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="86ea3-119">Interface</span></span>                                                  | <span data-ttu-id="86ea3-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86ea3-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86ea3-121">**Iamwmbufferpass**</span><span class="sxs-lookup"><span data-stu-id="86ea3-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="86ea3-122">Stellt eine Methode bereit, die es Anwendungen ermöglicht, sich für Rückrufe aus den Eingabe Pins des [WM-ASF-Writers](wm-asf-writer-filter.md) oder den Ausgabe Pins des WM-ASF- [Reader](wm-asf-reader-filter.md) -Filters zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="86ea3-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="86ea3-123">Wird bei der Indizierung und beim Hinzufügen von Dateneinheiten Erweiterungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="86ea3-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="86ea3-124">**Iamwmbufferpasscallback**</span><span class="sxs-lookup"><span data-stu-id="86ea3-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="86ea3-125">Wird von Anwendungen implementiert und von den Filtern aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="86ea3-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="86ea3-126">Anwendungen verwenden die eine Methode für diese Schnittstelle, um Informationen zu einzelnen Beispielen im Stream abzurufen.</span><span class="sxs-lookup"><span data-stu-id="86ea3-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="86ea3-127">Wird bei der Indizierung und beim Hinzufügen von Dateneinheiten Erweiterungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="86ea3-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="86ea3-128">[**Iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86ea3-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="86ea3-129">Implementiert auf dem WM-ASF-Writer.</span><span class="sxs-lookup"><span data-stu-id="86ea3-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="86ea3-130">Wird von Anwendungen verwendet, um Profile und Indizierungs Parameter für die Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="86ea3-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="86ea3-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86ea3-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="86ea3-132">Stellt zusätzliche Konfigurationsfunktionen für den WM-ASF-Writer bereit.</span><span class="sxs-lookup"><span data-stu-id="86ea3-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="86ea3-133">Die folgende Enumeration, Struktur und Ereignisse werden für die Verwendung mit den DirectShow-qasf-Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="86ea3-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="86ea3-134">Enumeration</span><span class="sxs-lookup"><span data-stu-id="86ea3-134">Enumeration</span></span>                                                               | <span data-ttu-id="86ea3-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86ea3-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ea3-136">[\_am \_ asfschreibconfig-Parameter \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86ea3-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="86ea3-137">Definiert Filter Konfigurationsparameter, die in den Methoden [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) und [**SetParam**](iconfigasfwriter2-setparam.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86ea3-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="86ea3-138">Struktur</span><span class="sxs-lookup"><span data-stu-id="86ea3-138">Structure</span></span>                                         | <span data-ttu-id="86ea3-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86ea3-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86ea3-140">**AM \_ WMT- \_ Ereignis \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="86ea3-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="86ea3-141">Enthält Informationen zu einem [**WMT- \_ Status**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) Ereignis und dem zugehörigen Status Code, der vom SDK für den Windows Media-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="86ea3-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="86ea3-142">Ereignis</span><span class="sxs-lookup"><span data-stu-id="86ea3-142">Event</span></span>                                           | <span data-ttu-id="86ea3-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86ea3-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86ea3-144">\_WMT- \_ Ereignis für EC</span><span class="sxs-lookup"><span data-stu-id="86ea3-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="86ea3-145">Das Ereignis wurde vom Windows Media-Format-SDK weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="86ea3-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="86ea3-146">EC \_ WMT- \_ Index \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="86ea3-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="86ea3-147">Wird gesendet, wenn eine Anwendung den [WM-ASF-Writer](wm-asf-writer-filter.md) zum Indizieren Windows Media Video Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="86ea3-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 