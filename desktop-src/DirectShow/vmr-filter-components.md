---
description: VMR-Filter Komponenten
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: VMR-Filter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529510"
---
# <a name="vmr-filter-components"></a>VMR-Filter Komponenten

Die VMR verwendet einen modularen Entwurf, der es Anwendungen ermöglicht, Sie für viele verschiedene renderingszenarios zu konfigurieren. Abhängig von der Konfiguration enthält VMR zwischen zwei und fünf unter Komponenten (zusätzlich zu den zugehörigen Eingabe Pins).

![VMR im Fenstermodus mit mehreren Streams](images/vmr-multiple-streams.png)

**Mixer:** Der Mixer ist ein COM-Objekt, das für das Mischen mehrerer Streams zuständig ist. Deinterlacing tritt auch innerhalb des Mischers auf. Der Mixer wird von VMR geladen, wenn mehrere Eingabestreams erkannt werden oder wenn das Eingabe Video mit Zeilen Sprung verknüpft ist. Der Mixer sammelt Informationen zu jedem Eingabedaten Strom und sortiert die Streams in der richtigen Z-Reihenfolge. Er ist dafür verantwortlich, zu bestimmen, wann jede Eingabe-PIN eine Stichprobe empfängt, und die Bildkomposition zum richtigen Zeitpunkt anzuweisen, die eigentliche Mischung auszuführen. Der Mixer berechnet auch den Zeitstempel, der auf jedes Ausgabe Bild angewendet werden soll. Wenn die Anwendung eine Bitmap bereitstellt, die oberhalb des zusammengesetzten Bilds angezeigt werden soll, ist der Mixer dafür verantwortlich, sicherzustellen, dass die Bitmap auch dann im oberen Bereich angezeigt wird, wenn die Z-Reihenfolge der Eingabedaten Ströme geändert wird.

**Bild Compositor:** Der Bild Compositor ist ein COM-Objekt, das die tatsächliche Mischung der Eingabedaten Ströme auf eine einzelne DirectDraw-oder Direct3D-Oberfläche durchführt, die von der Zuordnung-Presenter bereitgestellt wird. VMR bietet einen Standard-Bild Kompositions Tor, mit dem Anwendungen 2D-Alpha Mischungs Effekte durchführen können. Anwendungen können einen benutzerdefinierten Bild Compositor bereitstellen, um andere 2D-und 3D-Effekte zu ermöglichen, z. b. das Anwenden von Texturen auf Teile des Bilds, die Pixel Mischung pro Pixel, die Zuordnung des Bilds zum stationären oder das Verschieben von 3D-Objekten usw.

**Zuordnung-Presenter:** Der zuordnerpräsentator ist ein COM-Objekt, das das DirectDraw-oder Direct3D-Objekt zuordnet und die Kommunikation mit der Grafikkarte behandelt. Die Zeichnung kann entweder als kippen oder als Blit ausgeführt werden. Sie können Ihren eigenen Zuordnungs-Presenter einbinden, um das DirectDraw-oder Direct3D-Objekt zu erstellen und zu steuern und/oder um zur Präsentationszeit Zugriff auf die Video Bits zu erhalten.

**Fenster-Manager:** Der Fenster-Manager wird nur im Fenstermodus verwendet. Der Fenster-Manager unterstützt die Legacy-Schnittstellen [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) aus Gründen der Abwärtskompatibilität.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Video Mischungs Rendering](about-the-video-mixing-render.md)
</dt> </dl>

 

 



