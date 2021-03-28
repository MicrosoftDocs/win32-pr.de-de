---
description: Ebenso wie Kacheln nebeneinander nebeneinander angeordnet werden können, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel).
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Ticken einer Form mit einem Bild
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129061"
---
# <a name="tiling-a-shape-with-an-image"></a>Ticken einer Form mit einem Bild

Ebenso wie Kacheln nebeneinander nebeneinander angeordnet werden können, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel). Um das Innere einer Form zu Kacheln, verwenden Sie einen Textur Pinsel. Wenn Sie ein [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekt erstellen, ist eines der Argumente, die Sie an den Konstruktor übergeben, die Adresse eines [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts. Wenn Sie den Textur Pinsel verwenden, um das Innere einer Form zu zeichnen, wird die Form mit wiederholten Kopien dieses Bilds aufgefüllt.

Die Wrap Mode-Eigenschaft des [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekts bestimmt, wie das Bild ausgerichtet wird, da es in einem rechteckigen Raster wiederholt wird. Sie können festlegen, dass alle Kacheln im Raster die gleiche Ausrichtung aufweisen, oder Sie können das Bild von einer Raster Position zum nächsten kippen lassen. Die flippingoptionen können horizontal, vertikal oder beides sein. In den folgenden Beispielen wird das Ticken mit unterschiedlichen Arten von kippen veranschaulicht.

## <a name="tiling-an-image"></a>Ein Bild wird geziult.

In diesem Beispiel wird das folgende 75 × 75-Image zum Kacheln eines 200 × 200-Rechtecks verwendet:

![Abbildung, die als Grundlage für andere Abbildungen in diesem Thema verwendet wird: ein Haus und eine Baumstruktur im Hintergrund und zentriert in einem Rechteck](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass alle Kacheln die gleiche Ausrichtung aufweisen. Es gibt kein Flipping.

![Abbildung, die zeigt, wie das Basis Bild horizontal und vertikal in einem großen Rechteck wiederholt wird](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>Horizontales Kippen eines Bilds beim ticken

In diesem Beispiel wird ein 75 × 75-Bild zum Auffüllen eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild horizontal gekippt wird.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass das Bild beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile horizontal gekippt wird.

![Abbildung, die anzeigt, dass das Basis Bild horizontal wiederholt wird, aber gerade nummerierte Instanzen werden horizontal umgekehrt](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>Vertikales Kippen eines Bilds beim ticken

In diesem Beispiel wird ein 75 × 75-Bild zum Auffüllen eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild vertikal gedreht wird.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Spalte das Bild vertikal gekippt wird.

![die Abbildung zeigt, wie das Basis Bild horizontal und vertikal wiederholt wird, aber gerade nummerierte Zeilen werden vertikal umgekehrt.](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>Horizontales und vertikales Kippen eines Bilds beim ticken

In diesem Beispiel wird ein 75 × 75-Bild zum Kacheln eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild sowohl horizontal als auch vertikal gekippt wird.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



In der folgenden Abbildung wird gezeigt, wie das Rechteck durch das Bild gekachelt wird. Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile das Bild horizontal gekippt wird, und wenn Sie in einer bestimmten Spalte von einer Kachel zum nächsten wechseln, wird das Bild vertikal gekippt.

![die Abbildung zeigt, dass abwechselnde Instanzen des Basis Bilds in jeder Zeile horizontal gekippt werden und abwechselnde Zeilen vertikal gekippt werden.](images/tile5.png)

 

 



