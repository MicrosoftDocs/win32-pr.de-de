---
description: Verwenden des DirectShow EVR-Filters
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Verwenden des DirectShow EVR-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc454b6d298546afdbb5a06b7081505d9ddd7c2ab87a816e79bdb13836e9a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737313"
---
# <a name="using-the-directshow-evr-filter"></a>Verwenden des DirectShow EVR-Filters

Rufen Sie **CoCreateInstance** auf, um den filter enhanced video renderer (EVR) zu erstellen. Die CLSID ist CLSID \_ EnhancedVideoRenderer, definiert in uuids.h. Sie müssen [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) oder [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) nicht aufrufen, um den EVR-Filter zu verwenden.

Weitere Informationen zur Verwendung des EVR-Filters in einer DirectShow-Anwendung finden Sie unter [Audio-/Videowiedergabe in DirectShow.](../directshow/audio-video-playback-in-directshow.md)

Der EVR-Filter beginnt mit einem Eingabepin, der dem Verweisstream entspricht. Um Pins für Substreams hinzuzufügen, fragen Sie den Filter für die [**IEVRFilterConfig-Schnittstelle**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) ab, und rufen [**Sie IEVRFilterConfig::SetNumberOfStreams auf.**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) Rufen Sie diese Methode auf, bevor Sie eine Verbindung mit Eingabepins herstellen. Pin 0 ist immer der Verweisstream. Verbinden diesen Pin vor allen anderen Pins, da das Format des Verweisstreams einschränken kann, welche Unterstreamformate verfügbar sind.

Legen Sie vor dem Starten des Diagramms das Videoclipfenster und das Zielrechteck fest. Weitere Informationen finden Sie unter [Verwenden der Videoanzeigesteuerelemente.](using-the-video-display-controls.md)

Im Gegensatz zum Video Mixing Renderer (VMR) verfügt die EVR nicht über Betriebsmodi (fensterlos, fensterlos usw.). Dies gilt insbesondere für:

-   Der EVR unterstützt den Fenstermodus nicht. Die Anwendung muss das Ausschneidefenster bereitstellen.
-   Die EVR verfügt nicht über einen renderlosen Modus. Rufen Sie ZUM Ersetzen des Standardpräsentierers [**DIE AUFFORDERUNGVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)auf.
-   Die EVR verfügt nicht über einen Gemischtmodus. Die EVR erstellt immer den Mixer. Wenn Sie über einen Eingabestream verfügen, ist es nicht erforderlich, [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) aufzurufen, um die EVR zur Verwendung des Mixers zu zwingen.

## <a name="filter-interfaces"></a>Filterschnittstellen

Der EVR-Filter macht die folgenden Schnittstellen verfügbar. Einige dieser Schnittstellen sind im DirectShow SDK dokumentiert. Verwenden Sie **QueryInterface,** um Zeiger auf diese Schnittstellen abzurufen:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**DINNERVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **Ipersiststream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **Ispecifypropertypages**

## <a name="input-pin-interfaces"></a>Eingabe-Pin-Schnittstellen

Die Eingabepins im EVR-Filter machen die folgenden Schnittstellen verfügbar. Verwenden Sie **QueryInterface,** um Zeiger auf diese Schnittstellen abzurufen:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Darüber hinaus können Sie mithilfe der [**INTERFACESGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) die folgende Schnittstelle abrufen:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe in DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 
