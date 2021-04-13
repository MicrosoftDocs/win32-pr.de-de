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
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Entwickeln von Filter Diagrammen in DRM-Enabled Anwendungen

Wenn Ihre DirectShow-Anwendung die Wiedergabe von DRM-geschützten Dateien unterstützt, sollten Sie in der Regel **RenderFile** nicht zum Erstellen des Filter Diagramms verwenden, da es keine Möglichkeit gibt, anzugeben, welche DRM-Rechte Sie anfordern, bevor die Datei geöffnet wird. Der WM-ASF-Reader fordert standardmäßig nur Wiedergabe Rechte an. Der Filter wird dem Diagramm nicht hinzugefügt und kann daher von Anwendungen nicht gefunden werden, bis eine Datei erfolgreich geöffnet wird.

Zum Erstellen eines DRM-fähigen Wiedergabe Diagramms mithilfe des [WM-ASF-Readers](wm-asf-reader-filter.md)müssen Sie den Filter mithilfe von **cokreateinstance** instanziieren, ihn mithilfe von **igraphbuilder:: AddFilter** dem Filter Diagramm hinzufügen, ihn konfigurieren und dann seine Ausgabe Pins rendern. Dieses Verfahren wird im playwndasf-Beispiel veranschaulicht. Wenn Sie das Diagramm auf diese Weise erstellen, verfügen Sie bereits über den **ibasefilter** -Zeiger, der zum Abrufen von **iwmdrmwriter** zum Abrufen von " **QueryService** " verwendet werden kann. Diese Schnittstelle ist jedoch erst verfügbar, wenn das Windows Media Format SDK Reader-Objekt intern vom WM-ASF-Reader erstellt wird. Die erste Gelegenheit, dass die Anwendung DRM-Rechte festlegen muss, ist der WMT \_ No \_ Rights \_ Ex-Ereignishandler, wie im folgenden Code Ausschnitt gezeigt:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**Iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




