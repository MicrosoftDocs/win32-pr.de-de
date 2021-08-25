---
description: Ebenso wie Kacheln nebeneinander platziert werden können, um einen Boden abzudecken, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel).
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Kacheln einer Form mit einem Bild
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fc04439db21191ddc110859ae628e975d50bf617db3da63189859070766b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943770"
---
# <a name="tiling-a-shape-with-an-image"></a>Kacheln einer Form mit einem Bild

Ebenso wie Kacheln nebeneinander platziert werden können, um einen Boden abzudecken, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel). Verwenden Sie einen Texturpinsel, um das Innere einer Form zu kacheln. Wenn Sie ein [**TextureBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) erstellen, ist eines der Argumente, die Sie an den Konstruktor übergeben, die Adresse eines [**Image-Objekts.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Wenn Sie den Texturpinsel verwenden, um das Innere einer Form zu zeichnen, wird die Form mit wiederholten Kopien dieses Bilds gefüllt.

Die Wrapmoduseigenschaft des [**TextureBrush-Objekts**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) bestimmt, wie das Bild ausgerichtet ist, während es in einem rechteckigen Raster wiederholt wird. Sie können dafür sorgen, dass alle Kacheln im Raster die gleiche Ausrichtung haben, oder Sie können das Bild von einer Rasterposition zur nächsten drehen lassen. Das Flipping kann horizontal, vertikal oder beides sein. In den folgenden Beispielen wird das Kacheln mit verschiedenen Flippingtypen veranschaulicht.

## <a name="tiling-an-image"></a>Kacheln eines Bilds

In diesem Beispiel wird das folgende 75 ×75-Bild verwendet, um ein 200-×200-Rechteck zu kacheln:

![Abbildung, die als Grundlage für andere Abbildungen in diesem Thema verwendet wird: ein Haus und eine Struktur im Hintergrund und zentriert in einem Rechteck](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Die folgende Abbildung zeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass alle Kacheln die gleiche Ausrichtung haben. es gibt kein Flipping.

![Abbildung, die zeigt, dass das Basisbild horizontal und vertikal in einem großen Rechteck wiederholt wird](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling&quot;></a>Horizontales Drehen eines Bilds während der Kachel

In diesem Beispiel wird ein 75 ×75-Bild verwendet, um ein 200-×200-Rechteck auszufüllen. Der Umbruchmodus ist so festgelegt, dass das Bild horizontal gekippt wird.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Die folgende Abbildung zeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass das Bild horizontal gekippt wird, wenn Sie in einer bestimmten Zeile von einer Kachel zur nächsten wechseln.

![Abbildung, die zeigt, dass das Basisbild horizontal wiederholt wird, aber gerade nummerierte Instanzen horizontal umgekehrt werden](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling&quot;></a>Vertikales Drehen eines Bilds während der Kachel

In diesem Beispiel wird ein 75 ×75-Bild verwendet, um ein 200-×200-Rechteck auszufüllen. Der Umbruchmodus ist so festgelegt, dass das Bild vertikal gekippt wird.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Die folgende Abbildung zeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass das Bild vertikal gekippt wird, wenn Sie in einer bestimmten Spalte von einer Kachel zur nächsten wechseln.

![Abbildung, die zeigt, dass das Basisbild horizontal und vertikal wiederholt wird, aber gerade nummerierte Zeilen vertikal umgekehrt werden](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling&quot;></a>Horizontales und vertikales Drehen eines Bilds während der Kachel

In diesem Beispiel wird ein 75 ×75-Bild verwendet, um ein 200-×200-Rechteck zu kacheln. Der Umbruchmodus ist so festgelegt, dass das Bild horizontal und vertikal gekippt wird.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Die folgende Abbildung zeigt, wie das Rechteck vom Bild gekachelt wird. Beachten Sie, dass beim Verschieben von einer Kachel zur nächsten in einer bestimmten Zeile das Bild horizontal gekippt wird, und wenn Sie in einer bestimmten Spalte von einer Kachel zur nächsten wechseln, wird das Bild vertikal gekippt.

![Abbildung, die zeigt, dass abwechselnde Instanzen des Basisbilds in jeder Zeile horizontal und abwechselnde Zeilen vertikal gekippt werden](images/tile5.png)

 

 



