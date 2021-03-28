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
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="b85f5-103">Ticken einer Form mit einem Bild</span><span class="sxs-lookup"><span data-stu-id="b85f5-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="b85f5-104">Ebenso wie Kacheln nebeneinander nebeneinander angeordnet werden können, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel).</span><span class="sxs-lookup"><span data-stu-id="b85f5-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="b85f5-105">Um das Innere einer Form zu Kacheln, verwenden Sie einen Textur Pinsel.</span><span class="sxs-lookup"><span data-stu-id="b85f5-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="b85f5-106">Wenn Sie ein [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekt erstellen, ist eines der Argumente, die Sie an den Konstruktor übergeben, die Adresse eines [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts.</span><span class="sxs-lookup"><span data-stu-id="b85f5-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="b85f5-107">Wenn Sie den Textur Pinsel verwenden, um das Innere einer Form zu zeichnen, wird die Form mit wiederholten Kopien dieses Bilds aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b85f5-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="b85f5-108">Die Wrap Mode-Eigenschaft des [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekts bestimmt, wie das Bild ausgerichtet wird, da es in einem rechteckigen Raster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="b85f5-109">Sie können festlegen, dass alle Kacheln im Raster die gleiche Ausrichtung aufweisen, oder Sie können das Bild von einer Raster Position zum nächsten kippen lassen.</span><span class="sxs-lookup"><span data-stu-id="b85f5-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="b85f5-110">Die flippingoptionen können horizontal, vertikal oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="b85f5-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="b85f5-111">In den folgenden Beispielen wird das Ticken mit unterschiedlichen Arten von kippen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b85f5-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="b85f5-112">Ein Bild wird geziult.</span><span class="sxs-lookup"><span data-stu-id="b85f5-112">Tiling an Image</span></span>

<span data-ttu-id="b85f5-113">In diesem Beispiel wird das folgende 75 × 75-Image zum Kacheln eines 200 × 200-Rechtecks verwendet:</span><span class="sxs-lookup"><span data-stu-id="b85f5-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![Abbildung, die als Grundlage für andere Abbildungen in diesem Thema verwendet wird: ein Haus und eine Baumstruktur im Hintergrund und zentriert in einem Rechteck](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="b85f5-115">In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="b85f5-116">Beachten Sie, dass alle Kacheln die gleiche Ausrichtung aufweisen. Es gibt kein Flipping.</span><span class="sxs-lookup"><span data-stu-id="b85f5-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![Abbildung, die zeigt, wie das Basis Bild horizontal und vertikal in einem großen Rechteck wiederholt wird](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="b85f5-118">Horizontales Kippen eines Bilds beim ticken</span><span class="sxs-lookup"><span data-stu-id="b85f5-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="b85f5-119">In diesem Beispiel wird ein 75 × 75-Bild zum Auffüllen eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85f5-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="b85f5-120">Der Umbruch Modus ist so festgelegt, dass das Bild horizontal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="b85f5-121">In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="b85f5-122">Beachten Sie, dass das Bild beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile horizontal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![Abbildung, die anzeigt, dass das Basis Bild horizontal wiederholt wird, aber gerade nummerierte Instanzen werden horizontal umgekehrt](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="b85f5-124">Vertikales Kippen eines Bilds beim ticken</span><span class="sxs-lookup"><span data-stu-id="b85f5-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="b85f5-125">In diesem Beispiel wird ein 75 × 75-Bild zum Auffüllen eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85f5-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="b85f5-126">Der Umbruch Modus ist so festgelegt, dass das Bild vertikal gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="b85f5-127">In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="b85f5-128">Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Spalte das Bild vertikal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![die Abbildung zeigt, wie das Basis Bild horizontal und vertikal wiederholt wird, aber gerade nummerierte Zeilen werden vertikal umgekehrt.](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="b85f5-130">Horizontales und vertikales Kippen eines Bilds beim ticken</span><span class="sxs-lookup"><span data-stu-id="b85f5-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="b85f5-131">In diesem Beispiel wird ein 75 × 75-Bild zum Kacheln eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85f5-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="b85f5-132">Der Umbruch Modus ist so festgelegt, dass das Bild sowohl horizontal als auch vertikal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="b85f5-133">In der folgenden Abbildung wird gezeigt, wie das Rechteck durch das Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="b85f5-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="b85f5-134">Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile das Bild horizontal gekippt wird, und wenn Sie in einer bestimmten Spalte von einer Kachel zum nächsten wechseln, wird das Bild vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="b85f5-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![die Abbildung zeigt, dass abwechselnde Instanzen des Basis Bilds in jeder Zeile horizontal gekippt werden und abwechselnde Zeilen vertikal gekippt werden.](images/tile5.png)

 

 



