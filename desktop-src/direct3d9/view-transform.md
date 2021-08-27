---
description: In diesem Abschnitt werden die grundlegenden Konzepte der Ansichtstransformation und Details zum Einrichten einer Ansichtstransformationsmatrix in einer Direct3D-Anwendung erläutert.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Ansichtstransformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb184cb75f84a1d28ed6f03f2e65113ea65292fd6ca1871d517d472614f64a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118530"
---
# <a name="view-transform-direct3d-9"></a>Ansichtstransformation (Direct3D 9)

In diesem Abschnitt werden die grundlegenden Konzepte der Ansichtstransformation und Details zum Einrichten einer Ansichtstransformationsmatrix in einer Direct3D-Anwendung erläutert.

Die Ansichtstransformation sucht den Betrachter im Raum und wandelt Scheitelräume in Kameraraum um. Im Kameraraum befindet sich die Kamera oder der Betrachter am Ursprung und sieht in der positiven Z-Richtung. Denken Sie daran, dass Direct3D ein linkshändiges Koordinatensystem verwendet, sodass z in einer Szene positiv ist. Die Ansichtsmatrix versetzt die Objekte in der Welt um die Position einer Kamera – den Ursprung des Kameraraums – und die Ausrichtung.

Es gibt viele Möglichkeiten, eine Ansichtsmatrix zu erstellen. In allen Fällen hat die Kamera eine logische Position und Ausrichtung im Weltraum, die als Ausgangspunkt zum Erstellen einer Ansichtsmatrix verwendet wird, die auf die Modelle in einer Szene angewendet wird. Die Ansichtsmatrix übersetzt und dreht Objekte, um sie in den Kameraraum zu platzieren, wo sich die Kamera am Ursprung befindet. Eine Möglichkeit zum Erstellen einer Ansichtsmatrix besteht in der Kombination einer Übersetzungsmatrix mit Drehungsmatrizen für jede Achse. Bei diesem Ansatz gilt die folgende allgemeine Matrixgleichung.

![Gleichung der Ansichtstransformation](images/viewtran.png)

In dieser Formel ist V die Ansichtsmatrix, die erstellt wird, T ist eine Übersetzungsmatrix, die Objekte in der Welt neu positioniert, und Rₓ bis R<sub>z</sub> sind Drehmatrizen, die Objekte entlang der x-, y- und z-Achse drehen. Die Übersetzungs- und Drehungsmatrizen basieren auf der logischen Position und Ausrichtung der Kamera im Weltraum. Wenn die logische Position der Kamera in der Welt also <10.20.100> liegt, besteht das Ziel der Übersetzungsmatrix im Verschieben von Objekten –10 Einheiten entlang der x-Achse, -20 Einheiten entlang der y-Achse und -100 Einheiten entlang der Z-Achse. Die Drehmatrizen in der Formel basieren auf der Ausrichtung der Kamera in Bezug darauf, wie stark die Achsen des Kameraraums aus der Ausrichtung mit dem Weltraum gedreht werden. Wenn die zuvor erwähnte Kamera beispielsweise nach unten zeigt, liegt ihre Z-Achse 90 Grad (Pi/2 Bogenmaß) nicht in Der z-Achse des Weltraums, wie in der folgenden Abbildung dargestellt.

![Abbildung des Ansichtsraums der Kamera im Vergleich zum Weltraum](images/camtop.png)

Die Drehungsmatrizen wenden Drehungen gleicher, aber umgekehrter Größe auf die Modelle in der Szene an. Die Ansichtsmatrix für diese Kamera umfasst eine Drehung von -90 Grad um die x-Achse. Die Drehungsmatrix wird mit der Übersetzungsmatrix kombiniert, um eine Ansichtsmatrix zu erstellen, mit der die Position und Ausrichtung der Objekte in der Szene so angepasst wird, dass ihre Oberseite der Kamera zu sehen ist, sodass sich die Kamera über dem Modell befindet.

## <a name="setting-up-a-view-matrix"></a>Einrichten einer Ansichtsmatrix

Die [**Hilfsfunktionen D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) und [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) erstellen eine Ansichtsmatrix basierend auf der Kameraposition und einem Blickpunkt.

Im folgenden Beispiel wird eine Ansichtsmatrix für linkshändige Koordinaten erstellt.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D verwendet die Welt- und Ansichtsmatrizen, um mehrere interne Datenstrukturen zu konfigurieren. Jedes Mal, wenn Sie eine neue Welt- oder Ansichtsmatrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Das häufige Festlegen dieser Matrizen ist rechenintensiv. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt verketten und Matrizen in einer Weltsichtmatrix anzeigen, die Sie als Weltmatrix festlegen, und dann die Ansichtsmatrix auf die Identität festlegen. Speichern Sie zwischengespeicherte Kopien einzelner Welten, und zeigen Sie Matrizen an, die Sie bei Bedarf ändern, verketteen und zurücksetzen können. Aus Gründen der Übersichtlichkeit wird diese Optimierung in den Beispielen nur selten verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 



