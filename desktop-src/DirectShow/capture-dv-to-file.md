---
description: DV in Datei erfassen
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: DV in Datei erfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341918"
---
# <a name="capture-dv-to-file"></a>DV in Datei erfassen

In diesem Abschnitt wird beschrieben, wie Sie ein digitales Video (DV) von einer DV-Kamera oder einem VTR-Band erfassen.

1.  Erstellen Sie eine Instanz des [msdv-Treiber](msdv-driver.md) Filters. Weitere Informationen finden Sie unter [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md).
2.  Initialisieren Sie den Erfassungs Diagramm-Generator, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.
3.  Erstellen Sie das Erfassungs Diagramm, abhängig vom Ziel Dateityp:
    -   [Erfassen einer DV-Datei vom Typ "1"](capture-a-type-1-dv-file.md)
    -   [Erfassung einer Type-2-DV-Datei](capture-a-type-2-dv-file.md)
    -   [DV in nicht komprimiertem RGB erfassen](capture-dv-to-uncompressed-rgb.md)
4.  Führen Sie das Diagramm aus.

Die Erfassung von einem VTR-Band funktioniert genauso wie das Aufzeichnen von Livevideos von der Kamera, mit dem Unterschied, dass Sie das Band wie unter [Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)beschrieben abspielen müssen. Um den Verlust von Frames zu vermeiden, führen Sie zuerst das Diagramm aus, und geben Sie dann das Band wieder. Wenn Sie die Übertragung abgeschlossen haben, beenden Sie das Band zuerst, und beenden Sie dann das Diagramm.

> [!Note]  
> Der Camcorder muss sich im VTR-Modus befinden. Siehe [Geräte Modus](device-mode.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Type-1 im Vergleich zu Type-2 DV AVI-Dateien](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



