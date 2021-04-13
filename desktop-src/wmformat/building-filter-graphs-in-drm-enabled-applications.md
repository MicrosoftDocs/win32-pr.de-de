---
title: Entwickeln von Filter Diagrammen in DRM-Enabled Anwendungen
description: Entwickeln von Filter Diagrammen in DRM-Enabled Anwendungen
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media-Format-SDK, Bausteine von Filter Diagrammen
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, DRM-fähige Anwendungen
- Advanced Systems Format (ASF), Aufbau von Filter Diagrammen
- ASF (Advanced Systems Format), Bausteine von Filter Diagrammen
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), DRM-aktivierte Anwendungen
- ASF (Advanced Systems Format), DRM-aktivierte Anwendungen
- DirectShow, Bausteine von Filter Diagrammen
- DirectShow, DRM-fähige Anwendungen
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
- Digital Rights Management (DRM), Bausteine von Filter Diagrammen
- DRM (Digital Rights Management), Bausteine von Filter Diagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314332"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="99c4d-118">Entwickeln von Filter Diagrammen in DRM-Enabled Anwendungen</span><span class="sxs-lookup"><span data-stu-id="99c4d-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="99c4d-119">Wenn Ihre DirectShow-Anwendung die Wiedergabe von DRM-geschützten Dateien unterstützt, sollten Sie in der Regel **RenderFile** nicht zum Erstellen des Filter Diagramms verwenden, da es keine Möglichkeit gibt, anzugeben, welche DRM-Rechte Sie anfordern, bevor die Datei geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="99c4d-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="99c4d-120">Der WM-ASF-Reader fordert standardmäßig nur Wiedergabe Rechte an.</span><span class="sxs-lookup"><span data-stu-id="99c4d-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="99c4d-121">Der Filter wird dem Diagramm nicht hinzugefügt und kann daher von Anwendungen nicht gefunden werden, bis eine Datei erfolgreich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="99c4d-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="99c4d-122">Zum Erstellen eines DRM-fähigen Wiedergabe Diagramms mithilfe des [WM-ASF-Readers](wm-asf-reader-filter.md)müssen Sie den Filter mithilfe von **cokreateinstance** instanziieren, ihn mithilfe von **igraphbuilder:: AddFilter** dem Filter Diagramm hinzufügen, ihn konfigurieren und dann seine Ausgabe Pins rendern.</span><span class="sxs-lookup"><span data-stu-id="99c4d-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="99c4d-123">Dieses Verfahren wird im playwndasf-Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="99c4d-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="99c4d-124">Wenn Sie das Diagramm auf diese Weise erstellen, verfügen Sie bereits über den **ibasefilter** -Zeiger, der zum Abrufen von **iwmdrmwriter** zum Abrufen von " **QueryService** " verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="99c4d-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="99c4d-125">Diese Schnittstelle ist jedoch erst verfügbar, wenn das Windows Media Format SDK Reader-Objekt intern vom WM-ASF-Reader erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="99c4d-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="99c4d-126">Die erste Gelegenheit, dass die Anwendung DRM-Rechte festlegen muss, ist der WMT \_ No \_ Rights \_ Ex-Ereignishandler, wie im folgenden Code Ausschnitt gezeigt:</span><span class="sxs-lookup"><span data-stu-id="99c4d-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="99c4d-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99c4d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99c4d-128">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="99c4d-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="99c4d-129">**DRM-Attribut Liste**</span><span class="sxs-lookup"><span data-stu-id="99c4d-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="99c4d-130">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="99c4d-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="99c4d-131">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="99c4d-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="99c4d-132">**Iwmdrmreader**</span><span class="sxs-lookup"><span data-stu-id="99c4d-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="99c4d-133">**Iwmdrmwriter**</span><span class="sxs-lookup"><span data-stu-id="99c4d-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




