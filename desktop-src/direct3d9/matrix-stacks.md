---
description: Die Hilfsprogrammbibliothek D3DX stellt die ID3DXMATRIXStack-Schnittstelle bereit.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Matrixstapel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a480236bc42142b725e232a9fb92807be73fb03097104a0cc4fc08643f4361af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044328"
---
# <a name="matrix-stacks-direct3d-9"></a>Matrixstapel (Direct3D 9)

Die Hilfsprogrammbibliothek D3DX stellt die [**ID3DXMATRIXStack-Schnittstelle**](id3dxmatrixstack.md) bereit. Sie stellt einen Mechanismus bereit, mit dem Matrizen auf einen Matrixstapel gepusht und daraus entfernt werden können. Die Implementierung eines Matrixstapels ist eine effiziente Möglichkeit, Matrizen beim Durchlaufen einer Transformationshierarchie nachzuverfolgen.

Die D3DX-Hilfsprogrammbibliothek verwendet einen Matrixstapel, um Transformationen als Matrizen zu speichern. Die verschiedenen Methoden der [**ID3DXMATRIXStack-Schnittstelle**](id3dxmatrixstack.md) befassen sich mit der aktuellen Matrix oder der Matrix, die sich oben auf dem Stapel befindet. Sie können die aktuelle Matrix mit der [**ID3DXMATRIXStack::LoadIdentity-Methode**](id3dxmatrixstack--loadidentity.md) löschen. Um explizit eine bestimmte Matrix anzugeben, die als aktuelle Transformationsmatrix geladen werden soll, verwenden Sie die [**ID3DXMATRIXStack::LoadMatrix-Methode.**](id3dxmatrixstack--loadmatrix.md) Anschließend können Sie entweder die [**ID3DXMATRIXStack::MultMatrix-Methode**](id3dxmatrixstack--multmatrix.md) oder die [**ID3DXMATRIXStack::MultMatrixLocal-Methode**](id3dxmatrixstack--multmatrixlocal.md) aufrufen, um die aktuelle Matrix mit der angegebenen Matrix zu multiplizieren.

Mit der [**ID3DXMATRIXStack::P op-Methode**](id3dxmatrixstack--pop.md) können Sie zur vorherigen Transformationsmatrix zurückkehren, und die [**ID3DXMATRIXStack::P ush-Methode**](id3dxmatrixstack--push.md) fügt dem Stapel eine Transformationsmatrix hinzu.

Die einzelnen Matrizen im Matrixstapel werden als homogene Matrizen dargestellt, die durch die D3DX-Hilfsprogrammbibliothek [**D3DXMATRIX-Struktur**](d3dxmatrix.md) definiert werden.

Die D3DX-Hilfsprogrammbibliothek stellt einen Matrixstapel über ein COM-Objekt (Component Object Model) bereit.

## <a name="implementing-a-scene-hierarchy"></a>Implementieren einer Szenenhierarchie

Ein Matrixstapel vereinfacht die Erstellung hierarchischer Modelle, bei denen komplizierte Objekte aus einer Reihe einfacherer Objekte erstellt werden.

Eine Szenen- oder Transformationshierarchie wird in der Regel durch eine Struktur von Strukturdaten dargestellt. Jeder Knoten in der Struktur der Struktur enthält eine Matrix. Eine bestimmte Matrix stellt die Änderung der Koordinatensysteme vom übergeordneten Knoten zum Knoten dar. Wenn Sie beispielsweise einen menschlichen Arm modellieren, können Sie die Hierarchie implementieren, die im folgenden Diagramm dargestellt ist.

![Diagramm der Hierarchie eines menschlichen Armes](images/stack1.png)

In dieser Hierarchie platziert die Body-Matrix den Text in der Welt. Die UpperArm-Matrix enthält die Drehung der Achse, die LowerArm-Matrix enthält die Drehung des Ellenbogens, und die Handmatrix enthält die Drehung des Handbands. Um zu bestimmen, wo die Hand relativ zur Welt ist, multiplizieren Sie alle Matrizen von Körper nach unten durch Hand zusammen.

Die vorherige Hierarchie ist zu einfach, da jeder Knoten nur über ein untergeordnetes Element verfügt. Wenn Sie beginnen, die Hand ausführlicher zu modellieren, fügen Sie wahrscheinlich Finger und einen Daumen hinzu. Jede Ziffer kann der Hierarchie als untergeordnete Elemente von Hand hinzugefügt werden, wie im folgenden Diagramm dargestellt.

![Diagramm der Hierarchie einer menschlichen Hand](images/stack2.png)

Wenn Sie den vollständigen Graphen des Arms in der Reihenfolge der tiefen ersten Tiefe durchlaufen ( so weit wie möglich einen Pfad nach unten durchlaufen, bevor Sie zum nächsten Pfad wechseln), um die Szene zu zeichnen, führen Sie eine Sequenz des segmentierten Renderings aus. Um z. B. die Hand und die Finger zu rendern, implementieren Sie das folgende Muster.

1.  Pushen Sie die Handmatrix auf den Matrixstapel.
2.  Zeichnen Sie die Hand.
3.  Pushen Sie die Thumb-Matrix auf den Matrixstapel.
4.  Zeichnen Sie den Daumen.
5.  Legen Sie die Thumb-Matrix vom Stapel ab.
6.  Drücken Sie die Finger-1-Matrix auf den Matrixstapel.
7.  Zeichnen Sie den ersten Finger.
8.  Pop the Finger 1 matrix off the stack.
9.  Drücken Sie die Finger 2-Matrix auf den Matrixstapel. Sie fahren auf diese Weise fort, bis alle Finger und der Daumen gerendert werden.

Nachdem Sie das Rendern der Finger abgeschlossen haben, würden Sie die Handmatrix aus dem Stapel popen.

Sie können diesen grundlegenden Prozess mit den folgenden Beispielen im Code ausführen. Wenn sie während der tiefen ersten Suche der Struktur der Struktur auf einen Knoten stoßen, pushen Sie die Matrix an den oberen Rand des Matrixstapels.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Wenn Sie mit einem Knoten fertig sind, legen Sie die Matrix am oberen Rand des Matrixstapels ab.


```
MatrixStack->Pop();
```



Auf diese Weise stellt die Matrix oben im Stapel immer die Welttransformation des aktuellen Knotens dar. Daher sollten Sie vor dem Zeichnen der einzelnen Knoten die Direct3D-Matrix festlegen.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Weitere Informationen zu den spezifischen Methoden, die Sie für einen D3DX-Matrixstapel ausführen können, finden Sie im Referenzthema [**ID3DXMATRIXStack.**](id3dxmatrixstack.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 



