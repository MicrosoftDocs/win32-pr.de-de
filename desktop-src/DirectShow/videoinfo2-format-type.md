---
description: VideoInfo2-Formattyp
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2-Formattyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349079"
---
# <a name="videoinfo2-format-type"></a>VideoInfo2-Formattyp

Der bevorzugte Medientyp einer Vorschau-PIN kann ein Typ mit einem [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format sein. Diese Format Struktur unterstützt besondere Features, wie z. b. Text-und Bildseiten Verhältnisse.

VMR-7 und VMR-9 unterstützen [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) direkt. Wenn Sie die VMR mit dem Decoder verbinden, wird das beste Format ausgehandelt. Der ältere Videorendererfilter unterstützt jedoch **VIDEOINFOHEADER2** nicht. Wenn Sie **VIDEOINFOHEADER2** -Format Typen mit dem Videorenderer-Filter verwenden möchten, müssen Sie den [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter in das Diagramm einfügen.

1.  Auflisten der bevorzugten Medientypen im Ausgabepin des Decoder-Filters unter Verwendung der [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.
2.  Überprüfen Sie den ersten Medientyp in der enumerationssequenz.
3.  Wenn der Formattyp **Format \_ VideoInfo2** ist, verbinden Sie die Ausgabe-PIN mit dem Überlagerungs-Mixer. Verbinden Sie dann den Overlay-Mixer mit dem Videorenderer. (Siehe [Video Port Pins](video-port-pins.md).)

Wenn Sie sich keine Gedanken über diese Features machen, müssen Sie den Overlay-Mixer nicht verwenden. Verbinden Sie den Decoder direkt mit dem Videorenderer, und stattdessen wird eine Verbindung mit einem [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format hergestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[Verwenden des Overlay-Mischers bei der Video Erfassung](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



