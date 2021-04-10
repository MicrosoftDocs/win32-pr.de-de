---
description: Die D3DX Utility Library stellt die ID3DXMATRIXStack-Schnittstelle bereit.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Matrix Stapel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860318"
---
# <a name="matrix-stacks-direct3d-9"></a>Matrix Stapel (Direct3D 9)

Die D3DX Utility Library stellt die [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle bereit. Es stellt einen Mechanismus bereit, mit dem Matrizen auf einem Matrix Stapel abgelegt und aus diesem entfernt werden können. Das Implementieren eines Matrix Stapels ist eine effiziente Möglichkeit zum Nachverfolgen von Matrizen beim Durchlaufen einer Transformations Hierarchie.

Die D3DX Utility Library verwendet einen Matrix Stapel zum Speichern von Transformationen als Matrizen. Die verschiedenen Methoden der [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle befassen sich mit der aktuellen Matrix oder der Matrix, die sich über dem Stapel befindet. Sie können die aktuelle Matrix mit der [**ID3DXMATRIXStack:: loadidentity**](id3dxmatrixstack--loadidentity.md) -Methode löschen. Um explizit eine bestimmte Matrix anzugeben, die als aktuelle Transformationsmatrix geladen werden soll, verwenden Sie die [**ID3DXMATRIXStack:: loadmatrix**](id3dxmatrixstack--loadmatrix.md) -Methode. Anschließend können Sie entweder die [**ID3DXMATRIXStack:: mehrtmatrix**](id3dxmatrixstack--multmatrix.md) -Methode oder die [**ID3DXMATRIXStack:: multmatrixlocal**](id3dxmatrixstack--multmatrixlocal.md) -Methode aufzurufen, um die aktuelle Matrix mit der angegebenen Matrix zu multiplizieren.

Die [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) -Methode ermöglicht es Ihnen, zur vorherigen Transformationsmatrix zurückzukehren, und die [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) -Methode fügt dem Stapel eine Transformationsmatrix hinzu.

Die einzelnen Matrizen im Matrix Stapel werden als 4 x 4-Matrizen dargestellt, die von der D3DX Utility Library [**D3DXMATRIX**](d3dxmatrix.md) -Struktur definiert werden.

Die D3DX Utility Library bietet einen Matrix Stapel über ein COM-Objekt (Component Object Model).

## <a name="implementing-a-scene-hierarchy"></a>Implementieren einer Szenen Hierarchie

Ein Matrix Stapel vereinfacht die Erstellung von hierarchischen Modellen, in denen komplizierte Objekte aus einer Reihe von einfacheren Objekten erstellt werden.

Eine Szene-oder Transformations Hierarchie wird normalerweise durch eine Strukturdaten Struktur dargestellt. Jeder Knoten in der Strukturdaten Struktur enthält eine Matrix. Eine bestimmte Matrix stellt die Änderung in Koordinatensystemen zwischen dem übergeordneten Knoten des Knotens und dem Knoten dar. Wenn Sie z. b. eine menschliche Arm modellieren, können Sie die Hierarchie implementieren, die in der folgenden Abbildung dargestellt ist.

![Diagramm der Hierarchie einer menschlichen Arm](images/stack1.png)

In dieser Hierarchie platziert die Text Matrix den Text der Welt. Die Upperarm-Matrix enthält die Drehung der Schulter, die lowerarm-Matrix enthält die Drehung des Bogens, und die Hand Matrix enthält die Drehung des Handgelenks. Um zu ermitteln, wo sich die Hand in Bezug auf die Welt befindet, Multiplizieren Sie alle Matrizen vom Text nach unten.

Die vorherige Hierarchie ist übermäßig simpel, da jeder Knoten nur über ein untergeordnetes Element verfügt. Wenn Sie die Hand ausführlicher modellieren, werden Sie wahrscheinlich Finger und ein Thumb-Steuer Punkt hinzufügen. Jede Ziffer kann der Hierarchie als untergeordnete Elemente hinzugefügt werden, wie im folgenden Diagramm dargestellt.

![Diagramm der Hierarchie einer Menschenhand](images/stack2.png)

Wenn Sie das vollständige Diagramm des Arm-nach-oben-nach-unten-Reihenfolge durchlaufen, bevor Sie mit dem nächsten Pfad fortfahren, um die Szene zu zeichnen, führen Sie eine Sequenz segmentierter Rendering aus. Um z. b. die Hand und die Finger zu erzeugen, implementieren Sie das folgende Muster.

1.  Überträgt die Hand Matrix auf den Matrix Stapel.
2.  Zeichnen Sie die Hand.
3.  Übertragung der Ziehpunkt Matrix auf den Matrix Stapel.
4.  Ziehen Sie den Ziehpunkt.
5.  Blättern Sie die Ziehpunkt Matrix aus dem Stapel.
6.  Übertragung der Finger 1-Matrix auf den Matrix Stapel.
7.  Zeichnen Sie den ersten Finger.
8.  Schalten Sie die Finger 1-Matrix aus dem Stapel.
9.  Übertragung der Finger 2-Matrix auf den Matrix Stapel. Sie werden auf diese Weise fortgesetzt, bis alle Finger und Thumb gerendert werden.

Nachdem Sie das Rendering der Finger abgeschlossen haben, würden Sie die Hand Matrix aus dem Stapel aufklappen.

Sie können diesen grundlegenden Prozess in Code mit den folgenden Beispielen ausführen. Wenn während der tiefen Suche der Strukturdaten Struktur ein Knoten angezeigt wird, verschieben Sie die Matrix an den oberen Rand des Matrix Stapels.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Wenn Sie mit einem Knoten fertig sind, können Sie die Matrix am oberen Rand des Matrix Stapels aufklappen.


```
MatrixStack->Pop();
```



Auf diese Weise stellt die Matrix am Anfang des Stapels immer die weltweite Transformation des aktuellen Knotens dar. Vor dem Zeichnen der einzelnen Knoten sollten Sie daher die Direct3D-Matrix festlegen.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Weitere Informationen zu den spezifischen Methoden, die Sie für einen D3DX-Matrix Stapel ausführen können, finden Sie im [**ID3DXMATRIXStack**](id3dxmatrixstack.md) Reference Topic.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 



