---
description: Erfassen von DV in einer Datei
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Erfassen von DV in einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d886b964502d705f5902c17de8e6e008a11a31699de40b3089033867873fa021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814340"
---
# <a name="capture-dv-to-file"></a>Erfassen von DV in einer Datei

In diesem Abschnitt wird beschrieben, wie Digitales Video (DV) von einer DV-Kamera oder einem VTR-Band erfasst wird.

1.  Erstellen Sie eine Instanz des [MSDV-Treiberfilters.](msdv-driver.md) Weitere Informationen finden Sie unter [Auswählen eines Erfassungsgeräts.](selecting-a-capture-device.md)
2.  Initialisieren Sie den Capture Graph Builder, wie unter [Informationen zum Capture Graph Builder beschrieben.](about-the-capture-graph-builder.md)
3.  Erstellen Sie das Erfassungsdiagramm abhängig vom Zieldateityp:
    -   [Erfassen einer Typ-1-DV-Datei](capture-a-type-1-dv-file.md)
    -   [Erfassen einer Typ-2-DV-Datei](capture-a-type-2-dv-file.md)
    -   [Erfassen von DV in unkomprimiertem RGB](capture-dv-to-uncompressed-rgb.md)
4.  Führen Sie das Diagramm aus.

Das Aufzeichnen von einem VTR-Band funktioniert genauso wie das Erfassen von Livevideos von der Kamera, mit der Ausnahme, dass Sie das Band wiederspielen müssen, wie unter [Steuern eines DV-Dvd beschrieben.](controlling-a-dv-camcorder.md) Um den Verlust von Frames zu vermeiden, führen Sie zuerst den Graphen aus, und geben Sie dann das Band wieder. Wenn Sie mit der Übertragung fertig sind, beenden Sie zuerst das Band, und beenden Sie dann das Diagramm.

> [!Note]  
> Der Kernel muss sich im VTR-Modus befinden. Weitere Informationen [finden Sie unter Gerätemodus](device-mode.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Type-1 im Vergleich zu Type-2 DV AVI-Dateien](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



