---
description: Übertragen von DV von einer Datei auf ein Band
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Übertragen von DV von einer Datei auf ein Band
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bcd7bf716466cda2fc23a03968da4a51c005070f885183390f944d14994ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086790"
---
# <a name="transmit-dv-from-file-to-tape"></a>Übertragen von DV von einer Datei auf ein Band

Das Übertragen von DV AVI-Dateien auf VTR-Band ist etwas komplizierter, da Dateien typ-1 oder type-2 sein können. Gehen Sie wie folgt vor, um eine DV-Datei auf Band zu übertragen:

1.  Erstellen Sie eine Instanz des [MSDV-Treiberfilters.](msdv-driver.md) Weitere Informationen finden Sie unter [Auswählen eines Erfassungsgeräts.](selecting-a-capture-device.md)
2.  Stellen Sie sicher, dass sich das Gerät im VTR-Modus befindet. Andernfalls können Sie nicht auf Band übertragen. Weitere Informationen [finden Sie unter Gerätemodus](device-mode.md).
3.  Initialisieren Sie den Capture Graph Builder, wie unter [Informationen zum Capture Graph Builder beschrieben.](about-the-capture-graph-builder.md)
4.  Erstellen Sie das Diagramm. Die Graphkonfiguration hängt vom DV-Dateityp ab:
    -   [Übertragen aus Typ-1-Datei](transmit-from-type-1-file.md)
    -   [Übertragen aus Typ-2-Datei](transmit-from-type-2-file.md)
5.  Stellen Sie das Gerät in den Modus zum Anhalten von Aufzeichnungen ein, wie unter [Steuern einer DV-Dvd beschrieben.](controlling-a-dv-camcorder.md)
6.  Halten Sie das Filterdiagramm an. Während das Filterdiagramm angehalten wird, sendet es einen fortlaufenden Stream, der den ersten Videoframe wiederholt.
7.  Um mit der Übertragung zu beginnen, setzen Sie das Gerät in den Datensatzmodus, und führen Sie dann das Filterdiagramm aus. Das Gerät benötigt eine bestimmte Zeit, bis der Aufzeichnungskopf aufzeichnen kann. Warten Sie also etwa zwei Sekunden, bevor Sie den Graphen ausführen. Dies kann zu einigen duplizierten Frames am Anfang des Bandes führen, stellt jedoch sicher, dass keine Daten verloren gehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



