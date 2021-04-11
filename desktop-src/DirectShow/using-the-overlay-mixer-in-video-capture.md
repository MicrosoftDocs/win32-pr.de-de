---
description: Verwenden des Overlay-Mischers bei der Video Erfassung
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Verwenden des Overlay-Mischers bei der Video Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042559"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Verwenden des Overlay-Mischers bei der Video Erfassung

Es gibt bestimmte Arten von Videos, die der [Videorenderer](video-renderer-filter.md) -Filter nicht Selbstanzeigen kann. In diesen Fällen muss der Videorenderer mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter arbeiten. Der Überlagerungs-Mixer verwaltet das Rendering, während der Videorenderer das Videofenster verwaltet. Der Überlagerungs Mixer ist in den folgenden Situationen erforderlich:

-   "Videoport"-Pins (VP). Wenn das Erfassungsgerät einen Videoport verwendet, verwaltet der Überlagerungs Mixer die Hardware Überlagerung.
-   Video mit Zeilen Sprung. Für ein Zeilen Sprung Video benötigt der Decoder ein [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format, das der Videorenderer nicht unterstützt.
-   Untertitel. Der Beschriftungs Text wird als 8-Bit-pro-Pixel-Bitmaps gerendert, das der Überlagerungs-Mixer auf das Video überlagert.

Die **RenderStream** -Methode des Capture Graph-Generators fügt den Überlagerungs-Mixer bei Bedarf ein. Wenn Sie das Diagramm erstellen, ohne den Erfassungs Diagramm-Generator zu verwenden, müssen Sie jedoch jede dieser Situationen überprüfen und den Überlagerungs Mixer selbst einfügen.

-   \[! Wichtig\]  
    > Wenn das Gerät über eine VP-Pin verfügt, müssen Sie den Überlagerungs-Mixer auch dann verbinden, wenn Sie in Ihrer Anwendung keine Vorschau Funktionalität benötigen. Mit einem Videoport sendet das Erfassungsgerät die Videodaten immer an die Hardware Überlagerung, sodass der Überlagerungs Mixer immer benötigt wird.

     

Die videomischungs-rendererfilter (VMR-7 und VMR-9) unterstützen beide Zeilen Sprung Videos und können geschlossene Beschriftungs Bitmaps in das primäre Video mischen. Wenn Sie den VMR für diese Szenarien verwenden, müssen Sie den Überlagerungs-Mixer nicht verwenden. VMR-9 unterstützt keine VP-Pin-Verbindungen. VMR-7 unterstützt VP-Pin-Verbindungen über den Video Port-Manager-Filter. Allerdings können Sie feststellen, dass einige Treiber nicht ordnungsgemäß mit dem Videoport-Manager funktionieren. Aus diesem Grund wird der Überlagerungs Mixer weiterhin für VP Pins empfohlen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[VideoPort-Pins](video-port-pins.md)
</dt> <dt>

[VideoInfo2-Formattyp](videoinfo2-format-type.md)
</dt> </dl>

 

 



