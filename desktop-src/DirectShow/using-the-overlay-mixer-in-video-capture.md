---
description: Verwenden des Overlay-Mixer in Video Capture
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Verwenden des Overlay-Mixer in Video Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ada11ca55009b3ad67ba80c82575ab2d9bdf5a7329a88157ed4e003eca74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651194"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Verwenden des Overlay-Mixer in Video Capture

Es gibt bestimmte Arten von Videos, die der [Videorendererfilter](video-renderer-filter.md) nicht allein anzeigen kann. In diesen Situationen muss der Videorenderer mit dem [Filter Overlay](overlay-mixer-filter.md) Mixer arbeiten. Der Overlay Mixer verwaltet das Rendering, während der Videorenderer das Videofenster verwaltet. Die Overlay Mixer ist in den folgenden Situationen erforderlich:

-   Pins für Videoports (VP). Wenn das Erfassungsgerät einen Videoport verwendet, verwaltet der Overlay-Mixer die Hardwareüberlagerung.
-   Interlaced-Video. Für Interlacingvideos erfordert der Decoder ein [**VIDEOINFOHEADER2-Format,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) das vom Videorenderer nicht unterstützt wird.
-   Untertitel. Der Beschriftungstext wird als Bitmaps mit 8 Bits pro Pixel gerendert, die Mixer dem Video überlagert werden.

Die RenderStream Graph methode  des Capture-Generators fügt die Overlay-Mixer bei Bedarf ein. Wenn Sie das Diagramm jedoch ohne Capture Graph Builder erstellen, müssen Sie jede dieser Situationen überprüfen und die Overlay-Mixer einfügen.

-   \[! Wichtig\]  
    > Wenn das Gerät über einen VP-Pin verfügt, müssen Sie die Overlay-Mixer selbst dann verbinden, wenn Sie keine Vorschaufunktionen in Ihrer Anwendung benötigen. Mit einem Videoport sendet das Erfassungsgerät die Videodaten immer an die Hardwareüberlagerung, sodass die Overlay-Mixer immer benötigt wird.

     

Die Filter für videomischen Renderer (VMR-7 und VMR-9) unterstützen interlaced-Videos und können Untertitelbitmaps mit dem primären Video mischen. Wenn Sie die VMR für diese Szenarien verwenden, müssen Sie die Overlay-Mixer. VMR-9 unterstützt keine VP-Pinverbindungen. VMR-7 unterstützt VP-Pinverbindungen über den Videoport-Manager-Filter. Es kann jedoch sein, dass einige Treiber mit dem Videoport-Manager nicht ordnungsgemäß funktionieren. Aus diesem Grund wird die Overlay-Mixer weiterhin für VP-Pins empfohlen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungsthemen](advanced-capture-topics.md)
</dt> <dt>

[Videoport-Pins](video-port-pins.md)
</dt> <dt>

[VideoInfo2-Formattyp](videoinfo2-format-type.md)
</dt> </dl>

 

 



