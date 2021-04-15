---
description: In diesem Abschnitt werden die grundlegenden Konzepte der Ansichts Transformation vorgestellt, und es wird erläutert, wie Sie eine Ansichts Transformationsmatrix in einer Direct3D-Anwendung einrichten.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Transformation anzeigen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521907"
---
# <a name="view-transform-direct3d-9"></a>Transformation anzeigen (Direct3D 9)

In diesem Abschnitt werden die grundlegenden Konzepte der Ansichts Transformation vorgestellt, und es wird erläutert, wie Sie eine Ansichts Transformationsmatrix in einer Direct3D-Anwendung einrichten.

Die Transformation "Ansicht" lokalisiert den Viewer im Raum und wandelt Vertices in den Kamerabereich um. Im Kamerabereich befindet sich die Kamera oder der Viewer am Ursprung und sucht in der positiven z-Richtung. Denken Sie daran, dass Direct3D ein Links händiges Koordinatensystem verwendet, sodass z in einer Szene positiv ist. In der Sicht Matrix werden die Objekte weltweit um die Position einer Kamera, den Ursprung des Kamera Raums und die Ausrichtung, verschoben.

Es gibt viele Möglichkeiten, eine Ansichts Matrix zu erstellen. In allen Fällen hat die Kamera eine logische Position und Orientierung im Raum der Welt, die als Ausgangspunkt verwendet wird, um eine Ansichts Matrix zu erstellen, die auf die Modelle in einer Szene angewendet wird. Die Ansichts Matrix übersetzt und rotiert Objekte, um Sie in den Kamerabereich zu platzieren, in dem sich die Kamera am Ursprung befindet. Eine Möglichkeit zum Erstellen einer Sicht Matrix besteht darin, eine Übersetzungs Matrix mit Rotations Matrizen für jede Achse zu kombinieren. Bei dieser Vorgehensweise gilt die folgende allgemeine Matrix Gleichung.

![Gleichung der Ansichts Transformation](images/viewtran.png)

In dieser Formel ist V die Ansichts Matrix, die erstellt wird, T ist eine Übersetzungs Matrix, die Objekte der Welt neu positioniert, und r ₓ bis r<sub>z</sub> sind Rotations Matrizen, die Objekte entlang der x-, y-und z-Achse drehen. Die Konvertierungs-und Rotations Matrizen basieren auf der logischen Position und Ausrichtung der Kamera im Raum. Wenn die logische Position der Kamera auf der Welt <10, 20100> ist, besteht das Ziel der Übersetzungs Matrix darin, Objekte-10 Einheiten entlang der x-Achse,-20 Einheiten entlang der y-Achse und-100-Einheiten entlang der z-Achse zu verschieben. Die Rotations Matrizen in der Formel basieren auf der Ausrichtung der Kamera, im Hinblick darauf, wie viel die Achsen des Kamera Raums aus der Ausrichtung mit dem Raum gedreht werden. Wenn z. b. die zuvor erwähnte Kamera gerade zeigt, ist die z-Achse 90 Grad (PI/2-Bogenmaß) außerhalb der Ausrichtung auf die z-Achse des Raum Raums, wie in der folgenden Abbildung dargestellt.

![Darstellung des Anzeige Raums der Kamera im Vergleich zum Raum](images/camtop.png)

Die Rotations Matrizen wenden Drehungen von gleicher, aber umgekehrter Größe auf die Modelle in der Szene an. Die Ansichts Matrix für diese Kamera umfasst eine Drehung von-90 Grad um die x-Achse. Die Rotations Matrix wird mit der Übersetzungs Matrix kombiniert, um eine Ansichts Matrix zu erstellen, mit der die Position und Ausrichtung der Objekte in der Szene angepasst werden, sodass ihre Oberseite mit der Kamera verknüpft ist. Dadurch wird die Darstellung der Kamera oberhalb des Modells dargestellt.

## <a name="setting-up-a-view-matrix"></a>Einrichten einer Ansichts Matrix

Die Hilfsfunktionen [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) und [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) erstellen eine Ansichts Matrix basierend auf der Kameraposition und einem Blickpunkt.

Im folgenden Beispiel wird eine Ansichts Matrix für Links gesteuerte Koordinaten erstellt.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D verwendet die "World"-und "View"-Matrizen zum Konfigurieren mehrerer interner Datenstrukturen. Jedes Mal, wenn Sie eine neue Welt-oder Sicht Matrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Das häufige Festlegen dieser Matrizen ist Rechenzeit aufwändig. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt und Matrizen in einer World-View-Matrix verketten, die Sie als Weltmatrix festlegen, und dann die Ansichts Matrix auf die Identität festlegen. Behalten Sie zwischengespeicherte Kopien der einzelnen Welt bei, und zeigen Sie Matrizen an, die Sie ändern, verketten und die World Matrix nach Bedarf zurücksetzen können. Aus Gründen der Übersichtlichkeit werden diese Optimierungen in den Beispielen selten eingesetzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 



