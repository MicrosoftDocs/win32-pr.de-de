---
description: VideoPort-Pins
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: VideoPort-Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866435"
---
# <a name="video-port-pins"></a>VideoPort-Pins

Ein Erfassungsgerät mit einem Hardware Videoport verwendet möglicherweise die Video Port Erweiterungen (VPE) in Microsoft® DirectX®. Wenn dies der Fall ist, hat der Erfassungs Filter eine videolport-PIN (VP). Keine Videodaten werden von der VP-Pin über das Filter Diagramm übertragen. Stattdessen werden Video Frames in der Hardware erstellt und direkt an den Videospeicher gesendet. Die VP-Pin ermöglicht das Senden von Steuerungs Nachrichten an die Hardware.

Es ist wichtig, dass Sie die VP-Pin verbinden, auch wenn Ihre Anwendung nur die Datei Erfassung ohne Vorschau ausführt. Wenn Sie die PIN nicht verbunden lassen, wird das Diagramm nicht ordnungsgemäß ausgeführt. Dies unterscheidet sich von Vorschau Pins, die nicht verbunden werden müssen.

Die verschiedenen DirectShow-Videorenderer stellen unterschiedliche Unterstützung für VP Pins bereit:

-   Videorenderer: Verbinden Sie die VP-PIN mit PIN 0 auf dem [Überlagerungs Mischungs](overlay-mixer-filter.md) Filter, und verbinden Sie den Überlagerungs Filter Filter mit dem Videorenderer.
-   VMR-7: Verbinden Sie die VP-PIN mit dem [Video Port-Manager](video-port-manager.md) -Filter, und verbinden Sie den Videoport-Manager mit VMR-7.
-   VMR-9: Sie können VMR-9 nicht verwenden, wenn das Gerät über eine VP-Pin verfügt, da Direct3D 9 keine videports unterstützt. Verwenden Sie entweder den Videorenderer oder VMR-7.

Für Video Port Szenarios werden der Überlagerungs-und Videorenderer über Video Port Manager und VMR-7 empfohlen, da nicht alle Treiber den Videoport-Manager unterstützen. Im Allgemeinen ist der Überlagerungs Mixer die zuverlässigste Option für videports.

Mit der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode wird der Überlagerungs-Mixer automatisch eingefügt, wenn eine VP-Pin vorhanden ist. Wenn Sie das Diagramm erstellen, ohne diese Methode zu verwenden, sollten Sie überprüfen, ob im Erfassungs Filter eine Videoport-Pin vorhanden ist. ist dies der Fall, stellen Sie eine Verbindung mit dem Filter für den Überlagerungs Filter her, wie im folgenden Diagramm dargestellt.

![Verbinden einer Videoport-PIN mit dem Überlagerungs-Mischungs Filter.](images/vidcap11.png)

Sie können die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode verwenden, um nach einer VP-PIN im Erfassungs Filter zu suchen:


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



Nachdem Sie den Overlay-Mixer dem Diagramm hinzugefügt haben, können Sie **findpin** erneut ausführen, um PIN 0 auf dem Überlagerungs Mixer zu suchen. PIN 0 ist immer die erste Eingabe-PIN für den Filter.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Verbinden Sie die beiden Pins durch Aufrufen von [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Verbinden Sie anschließend die Ausgabe-PIN des Overlay-Handlers mit dem Videorendererfilter. Sie können das Video ausblenden, indem Sie die sichtbaren Methoden [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) und [**IVideoWindow::p UT \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) im Filter Graph-Manager aufrufen.

Bei TV-Tuners kann der Erfassungs Filter auch eine Video Port-VBI-PIN (PIN- \_ Kategorie \_ Videoport \_ VBI) enthalten. Wenn dies der Fall ist, verbinden Sie diese PIN mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) . Weitere Informationen finden Sie unter [anzeigen](viewing-closed-captions.md)von Untertiteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[Verwenden des Overlay-Mischers bei der Video Erfassung](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



