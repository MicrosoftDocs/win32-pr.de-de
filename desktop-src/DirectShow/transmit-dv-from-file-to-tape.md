---
description: Übertragung von DV von Datei auf Band
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Übertragung von DV von Datei auf Band
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352246"
---
# <a name="transmit-dv-from-file-to-tape"></a>Übertragung von DV von Datei auf Band

Die Übertragung von der DV-AVI-Datei an das VTR-Band ist etwas komplizierter, da Dateien-1 oder Typ-2 eingeben können. Gehen Sie folgendermaßen vor, um eine DV-Datei an das Band zu übertragen:

1.  Erstellen Sie eine Instanz des [msdv-Treiber](msdv-driver.md) Filters. Weitere Informationen finden Sie unter [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md).
2.  Stellen Sie sicher, dass sich das Gerät im VTR-Modus befindet. Andernfalls können Sie nicht auf Band übertragen. Siehe [Geräte Modus](device-mode.md).
3.  Initialisieren Sie den Erfassungs Diagramm-Generator, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.
4.  Erstellen Sie das Diagramm. Die Diagramm Konfiguration hängt vom DV-Dateityp ab:
    -   [Übertragen von Datei vom Typ "-1"](transmit-from-type-1-file.md)
    -   [Übertragen von Typ-2-Datei](transmit-from-type-2-file.md)
5.  Versetzen Sie das Gerät in den Modus zum Anhalten des Einsatzes, wie unter [Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)beschrieben.
6.  Halten Sie das Filter Diagramm an. Während das Filter Diagramm angehalten wird, sendet es einen kontinuierlichen Stream, der den ersten Frame des Videos wiederholt.
7.  Um mit der Übertragung zu beginnen, versetzen Sie das Gerät in den Aufzeichnungsmodus und führen dann das Filter Diagramm aus. Das Gerät nimmt eine bestimmte Zeitspanne an, bis die Aufzeichnungs Kopfzeile aufzeichnen kann. warten Sie also ungefähr zwei Sekunden, bevor Sie das Diagramm ausführen. Dies führt möglicherweise zu einigen doppelten Frames am Anfang des Bands, stellt jedoch sicher, dass keine Daten verloren gehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



