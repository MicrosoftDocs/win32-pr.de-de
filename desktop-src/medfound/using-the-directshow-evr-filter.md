---
description: Verwenden des DirectShow-EVR-Filters
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Verwenden des DirectShow-EVR-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356637"
---
# <a name="using-the-directshow-evr-filter"></a>Verwenden des DirectShow-EVR-Filters

Um den EVR-Filter (Enhanced Video Renderer) zu erstellen, rufen Sie **cokreateinstance** auf. Die CLSID ist CLSID \_ enhancedvidederer, der in UUIDs. h definiert ist. Sie müssen [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) oder [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) nicht für die Verwendung des EVR-Filters anrufen.

Weitere Informationen zum Verwenden des EVR-Filters in einer DirectShow-Anwendung finden Sie unter [Audiowiedergabe und Video Wiedergabe in DirectShow](../directshow/audio-video-playback-in-directshow.md).

Der EVR-Filter beginnt mit einer Eingabe-PIN, die dem Verweis Datenstrom entspricht. Um Pins für unter Ströme hinzuzufügen, Fragen Sie den Filter nach der [**ievrfilterconfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) -Schnittstelle ab, und nennen Sie [**ievrfilterconfig:: setnumofstreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Nennen Sie diese Methode, bevor Sie eine Verbindung mit Eingabe Pins herstellen. PIN 0 ist immer der Verweis Datenstrom. Verbinden Sie diese Pin vor allen anderen Pins, da das Format des Verweis Datenstroms möglicherweise einschränkt, welche substreamformate verfügbar sind.

Legen Sie vor dem Starten des Diagramms das Video Clipping-Fenster und das Ziel Rechteck fest. Weitere Informationen finden Sie unter [Verwenden der Video Anzeige Steuerelemente](using-the-video-display-controls.md).

Im Gegensatz zum Video Mischungs-Renderer (VMR) verfügt der EVR nicht über Betriebsmodi (Fenster, fensterlose usw.). Dies gilt insbesondere für:

-   Der EVR unterstützt den Fenster-Modus nicht. Die Anwendung muss das clippingfenster bereitstellen.
-   Der EVR weist keinen renderlosen Modus auf. Um den Standard Presenter zu ersetzen, nennen Sie [**imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   Der EVR weist keinen Mischungs Modus auf. Der EVR erstellt immer den Mixer. Wenn Sie über einen Eingabestream verfügen, ist es nicht erforderlich, [**setnumofstreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) aufzurufen, um die Verwendung des Mixers durch den EVR zu erzwingen.

## <a name="filter-interfaces"></a>Filter Schnittstellen

Der EVR-Filter macht die folgenden Schnittstellen verfügbar. Einige dieser Schnittstellen sind im DirectShow SDK dokumentiert. Verwenden Sie **QueryInterface** zum Abrufen von Zeigern auf diese Schnittstellen:

-   [**Iamcertifiedoutputprotection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**Iamfilterfehlflags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**Ibasefilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**Ievrfilterconfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   " [**Ikspropertyset**](../directshow/ikspropertyset.md) " (DirectShow)
-   [**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**Imsvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**Iqualitycontrol**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**Iqualprop**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>PIN-Eingabeschnittstellen

Die Eingabe Pins im EVR-Filter machen die folgenden Schnittstellen verfügbar. Verwenden Sie **QueryInterface** zum Abrufen von Zeigern auf diese Schnittstellen:

-   [**Ievrvideostreamcontrol**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**Iqualitycontrol**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Außerdem können Sie die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle zum Abrufen der folgenden Schnittstelle verwenden:

-   [**Idirectxvideomemoryconfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiowiedergabe und Video Wiedergabe in DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 
