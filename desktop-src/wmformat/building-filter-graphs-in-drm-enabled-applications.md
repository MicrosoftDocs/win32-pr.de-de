---
title: Erstellen von Filterdiagrammen in DRM-Enabled Anwendungen
description: Erstellen von Filterdiagrammen in DRM-Enabled Anwendungen
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Medienformat-SDK, Erstellen von Filterdiagrammen
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, DRM-fähige Anwendungen
- Advanced Systems Format (ASF), Erstellen von Filterdiagrammen
- ASF (Advanced Systems Format), Erstellen von Filterdiagrammen
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), DRM-fähige Anwendungen
- ASF (Advanced Systems Format), DRM-fähige Anwendungen
- DirectShow,Erstellen von Filterdiagrammen
- DirectShow,DRM-fähige Anwendungen
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
- Digital Rights Management (DRM), Erstellen von Filterdiagrammen
- DRM (Digital Rights Management), Erstellen von Filterdiagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447950"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Erstellen von Filterdiagrammen in DRM-Enabled Anwendungen

Wenn Ihre DirectShow-Anwendung die Wiedergabe von DRM-geschützten Dateien unterstützt, sollten Sie im Allgemeinen **renderFile** nicht zum Erstellen des Filterdiagramms verwenden, da es keine Möglichkeit gibt, anzugeben, welche DRM-Rechte Sie vor dem Öffnen der Datei anfordern. Der WM ASF-Reader fordert standardmäßig nur Wiedergaberechte an. Der Filter wird dem Diagramm nicht hinzugefügt und kann daher erst von Anwendungen gefunden werden, wenn eine Datei erfolgreich geöffnet wurde.

Um ein DRM-fähiges Wiedergabediagramm mithilfe des [WM ASF-Readers](wm-asf-reader-filter.md)zu erstellen, müssen Sie den Filter mit **CoCreateInstance** instanziieren, ihn mithilfe von **IGraphBuilder::AddFilter** dem Filterdiagramm hinzufügen, ihn konfigurieren und dann seine Ausgabepins rendern. Diese Technik wird im PlayWndASF-Beispiel demonstriert. Wenn Sie das Diagramm auf diese Weise erstellen, verfügen Sie bereits über den **IBaseFilter-Zeiger,** mit dem QueryService aufgerufen werden **kann,** um **IWMDRMWriter zu erhalten.** Diese Schnittstelle ist jedoch erst verfügbar, wenn das Windows Media Format SDK-Readerobjekt intern vom WM ASF-Reader erstellt wurde. Die erste Gelegenheit, die die Anwendung zum Festlegen von DRM-Rechten hat, befindet sich im WMT \_ NO \_ RIGHTS EX-Ereignishandler, wie im folgenden \_ Codeausschnitt gezeigt:


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

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




