---
description: Videoport-Pins
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Videoport-Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94202e05cc467eabb77719a145a77310a62482e6f82772261b57e5ff544d2b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696784"
---
# <a name="video-port-pins"></a>Videoport-Pins

Ein Erfassungsgerät mit einem Hardwarevideoport kann die Videoporterweiterungen (VPE) in Microsoft® DirectX® verwenden. Wenn ja, verfügt der Erfassungsfilter über einen Videoport(VP)-Pin. Es werden keine Videodaten vom VP-Pin durch das Filterdiagramm bewegt. Stattdessen werden Videoframes auf Hardware erstellt und direkt an den Videospeicher gesendet. Der VP-Pin ermöglicht das Senden von Steuernachrichten an die Hardware.

Es ist wichtig, den VP-Pin zu verbinden, auch wenn Ihre Anwendung nur Dateierfassungen ohne Vorschau ausführt. Wenn Sie den Pin nicht verbunden lassen, wird das Diagramm nicht ordnungsgemäß ausgeführt. Dies unterscheidet sich von Vorschaupins, die nicht verbunden werden müssen.

Die verschiedenen DirectShow-Videorenderer bieten unterschiedliche Unterstützung für VP-Pins:

-   Videorenderer: Verbinden den VP-Pin an, um 0 an den [Filter Overlay Mixer](overlay-mixer-filter.md) anzuheften, und verbinden Sie den Filter Overlay Mixer mit dem Videorenderer.
-   VMR-7: Verbinden den VP-Pin an den [VideoPort-Manager-Filter](video-port-manager.md) an, und verbinden Sie den Videoport-Manager mit VMR-7.
-   VMR-9: Sie können die VMR-9 nicht verwenden, wenn das Gerät über einen VP-Pin verfügt, da Direct3D 9 keine Videoports unterstützt. Verwenden Sie entweder den Videorenderer oder VMR-7.

Für Videoportszenarien werden die Overlay-Mixer und der Videorenderer über den Videoport-Manager und VMR-7 empfohlen, da nicht alle Treiber den Videoport-Manager unterstützen. Im Allgemeinen ist overlay Mixer die zuverlässigste Option für Videoports.

Die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) fügt automatisch die Overlay-Mixer ein, wenn ein VP-Pin vorhanden ist. Wenn Sie das Diagramm ohne diese Methode erstellen, sollten Sie nach einer Videoport-Stecknadel für den Erfassungsfilter suchen. Wenn ein Diagramm vorhanden ist, stellen Sie eine Verbindung mit dem Filter Overlay Mixer her, wie im folgenden Diagramm dargestellt.

![Verbinden eines Videoportanschlusses mit dem Overlaymixerfilter.](images/vidcap11.png)

Sie können die [**ICaptureGraphBuilder2::FindPin-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) verwenden, um im Erfassungsfilter nach einem VP-Pin zu suchen:


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



Nachdem Sie dem Diagramm die Overlay-Mixer hinzugefügt haben, rufen **Sie erneut FindPin** auf, um pin 0 auf dem Overlay-Mixer zu suchen. Pin 0 ist immer der erste Eingabepin im Filter.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Verbinden die beiden Pins, indem [**Sie IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)aufrufen.


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Verbinden Sie dann den Ausgabepin des Overlay-Mixer mit dem Filter Videorenderer. Sie können das Video ausblenden, indem Sie die Methoden [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) und [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) im Filter Graph Manager aufrufen.

Für TV-Tuner verfügt der Erfassungsfilter möglicherweise auch über einen Videoport-VBI-Pin (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Wenn ja, verbinden Sie diesen Stecknadel mit dem [Filter VBI Surface Allocator.](vbi-surface-allocator.md) Weitere Informationen finden Sie unter [Anzeigen von Untertiteln.](viewing-closed-captions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Themen zur erweiterten Erfassung](advanced-capture-topics.md)
</dt> <dt>

[Verwenden des Overlay-Mixer in Video Capture](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



