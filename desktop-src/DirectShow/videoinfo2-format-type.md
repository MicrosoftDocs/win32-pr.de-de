---
description: VideoInfo2-Formattyp
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2-Formattyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071924"
---
# <a name="videoinfo2-format-type"></a>VideoInfo2-Formattyp

Der bevorzugte Medientyp eines Vorschaupins kann ein Typ mit dem Format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) sein. Diese Formatstruktur unterstützt spezielle Features, z. B. Seitenverhältnis zwischen Video und Bild.

SOWOHL VMR-7 als auch VMR-9 unterstützen [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) direkt. Wenn Sie die VMR mit dem Decoder verbinden, wird das beste Format ausgehandelt. Der ältere Videorendererfilter unterstützt **videoINFOHEADER2** jedoch nicht. Um **VIDEOINFOHEADER2-Formattypen** mit dem Videorendererfilter zu verwenden, müssen Sie das [Overlay Mixer](overlay-mixer-filter.md) Filter in das Diagramm einfügen.

1.  Aufzählen der bevorzugten Medientypen auf dem Ausgabepin des Decoderfilters mithilfe der [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)
2.  Überprüfen Sie den ersten Medientyp in der Enumerationssequenz.
3.  Wenn der Formattyp **FORMAT \_ VideoInfo2** lautet, verbinden Sie den Ausgabepin mit dem Overlay-Mixer. Verbinden Sie dann die Overlay-Mixer mit dem Videorenderer. (Weitere Informationen finden Sie unter [Videoport-Pins.)](video-port-pins.md)

Wenn Sie diese Features nicht interessieren, müssen Sie die Overlay-Mixer nicht verwenden. Verbinden den Decoder direkt an den Videorenderer und stellt stattdessen eine Verbindung mit einem [**VIDEOINFOHEADER-Format**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) her.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Themen zur erweiterten Erfassung](advanced-capture-topics.md)
</dt> <dt>

[Verwenden der Überlagerungs-Mixer in Video Capture](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



