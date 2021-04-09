---
title: DRM-Unterstützung in DirectShow
description: DRM-Unterstützung in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media-Format-SDK, DRM-Unterstützung in DirectShow
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Advanced Systems Format (ASF), DRM-Unterstützung in DirectShow
- ASF (Advanced Systems Format), DRM-Unterstützung in DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- DirectShow, DRM-Unterstützung
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948421"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="281a3-115">DRM-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="281a3-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="281a3-116">Das Lesen und Schreiben von DRM-geschützten Dateien in DirectShow erfolgt im Grunde auf die gleiche Weise wie bei der direkten Verwendung des Windows Media SDK-SDKs.</span><span class="sxs-lookup"><span data-stu-id="281a3-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="281a3-117">Zunächst benötigen Sie die statische wmstubdrm-Bibliothek, die separat von Microsoft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="281a3-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="281a3-118">Außerdem müssen Sie die **ikeyprovider** -Schnittstelle implementieren, damit Ihre Anwendung auf die Lauf Zeit Objekte des Windows Media-Formats zugreifen kann, wenn DRM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="281a3-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="281a3-119">Verwenden Sie beim Anwenden von DRM-Version 1-Schutz die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle, die wie unter [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)beschrieben abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="281a3-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="281a3-120">Wenn Sie den DRM-Schutz der Version 7 anwenden, rufen Sie die [**iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) -Schnittstelle ab, indem Sie **QueryService** für den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter aufrufen, wie im Code Ausschnitt weiter unten in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="281a3-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="281a3-121">Alle anderen DRM-spezifischen Konfigurationen sind exakt identisch mit der Beschreibung [unter Aktivieren der DRM-Unterstützung](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="281a3-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="281a3-122">Verwenden Sie **QueryService** , um die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle aus dem [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="281a3-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="281a3-123">DirectX 9,0 enthält ein Beispiel: playwndasf, eine DRM-fähige DirectShow Player-Anwendung, die DRM-Version 1 und den Lizenzerwerb von Version 7 veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="281a3-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="281a3-124">Dieses Beispiel enthält auch eine Implementierung der **ckeyprovider** -Klasse, die die **ikeyprovider** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="281a3-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




