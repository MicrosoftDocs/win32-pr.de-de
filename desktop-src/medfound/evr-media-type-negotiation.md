---
description: EVR-Medientypaushandlung
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR-Medientypaushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974489"
---
# <a name="evr-media-type-negotiation"></a>EVR-Medientypaushandlung

In diesem Thema wird beschrieben, wie der erweiterte Videorenderer (EVR) Medientypen überprüft.

-   Für den DirectShow EVR-Filter erfolgt die Typaushandlung, wenn die Pins des Filters verbunden sind.

-   Für die EVR-Mediensenke werden die Medientypen über die [**INTERFACESMediaTypeHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) in den Streamsenken festgelegt. In der Regel handelt das Topologieladeprogramm die Medientypen aus, obwohl die Anwendung die Medientypen auch direkt festlegen kann.

Die EVR meldet keine bevorzugten Medientypen. Der Client muss Medientypen testen, bis ein akzeptabler Typ gefunden wird. Der Medientyp für den Verweisstream muss festgelegt werden, bevor die Typen für einen der Unterstreams festgelegt werden können.

Für den Verweisstream ruft der EVR-Mixer eine Liste kompatibler DXVA-Renderzielformate (DirectX Video Acceleration) ab. Die EVR-Moderatorin verwendet diese Liste, um das Format für die Direct3D-Swapkette auszuwählen. Wenn kein kompatibles Renderzielformat gefunden werden kann, lehnt die EVR den Medientyp ab.

Für die Unterstreams fragt der EVR-Mixer ab, ob das DXVA-Gerät dieses Unterstreamformat in Kombination mit dem Renderzielformat unterstützt, das für den Verweisstream ausgewählt wurde. Daher können sich die verfügbaren Unterstreamformate je nach Verweisstream ändern.

Hier ist der Prozess ausführlicher. Diese Details sind für die meisten Anwendungen nicht wichtig, können aber hilfreich sein, wenn Sie einen benutzerdefinierten Mixer oder Presenter schreiben.

Für den Verweisstream erfolgt die Aushandlung wie folgt:

1.  Der EVR ruft [**AUFTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.

2.  Der Mixer konvertiert den Medientyp unter Verwendung der [**DXVA2 \_ VideoDesc-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) in eine DXVA 2.0-Beschreibung.

3.  Der Mixer ruft [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) auf, um eine Liste der Videoprozessor-GUIDs abzurufen.

4.  Für jede Videoprozessor-GUID ruft der Mixer [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) auf, um die unterstützten Renderzielformate abzurufen.

5.  Der EVR ruft [**AUFANZEIGEVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) auf dem Presenter mit der \_ MFVP MESSAGE \_ INVALIDATEMEDIATYPE-Nachricht auf. Diese Meldung bewirkt, dass die Präsentation ein neues Format auswählt.

6.  Der Presenter ruft [**DIE AUSGABETRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine Liste der verfügbaren Ausgabeformate vom Mixer abzurufen. Der Mixer generiert diese Liste aus den in Schritt 4 abgerufenen Formaten.

7.  Der Presenter wählt ein Format aus und ruft [**AUFTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf dem Mixer auf.

Bei Unterstreams ist der Prozess einfacher:

1.  Der EVR ruft [**AUFTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.

2.  Der Mixer ruft [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) auf, um eine Liste der verfügbaren Unterstreamformate abzurufen.

3.  Wenn das vorgeschlagene Format in dieser Liste enthalten ist, akzeptiert die EVR den Eingabetyp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



