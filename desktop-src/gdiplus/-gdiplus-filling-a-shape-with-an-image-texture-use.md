---
description: Sie können eine geschlossene Form mit einer Textur auffüllen, indem Sie die Image-Klasse und die TextureBrush-Klasse verwenden.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Auffüllen einer Form mit einer Bildstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131341"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="88b30-103">Auffüllen einer Form mit einer Bildstruktur</span><span class="sxs-lookup"><span data-stu-id="88b30-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="88b30-104">Sie können eine geschlossene Form mit einer Textur auffüllen, indem Sie die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse und die [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="88b30-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="88b30-105">Im folgenden Beispiel wird eine Ellipse mit einem Bild gefüllt.</span><span class="sxs-lookup"><span data-stu-id="88b30-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="88b30-106">Der Code erstellt ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und übergibt dann die Adresse dieses **Bild** Objekts als Argument an einen [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="88b30-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="88b30-107">Die dritte Code Anweisung skaliert das Bild, und die vierte Anweisung füllt die Ellipse mit wiederholten Kopien des skalierten Bilds:</span><span class="sxs-lookup"><span data-stu-id="88b30-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="88b30-108">Im vorangehenden Codebeispiel legt die [**TextureBrush:: setTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) -Methode die Transformation fest, die auf das Bild angewendet wird, bevor Sie gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="88b30-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="88b30-109">Angenommen, das ursprüngliche Bild hat eine Breite von 640 Pixeln und eine Höhe von 480 Pixel.</span><span class="sxs-lookup"><span data-stu-id="88b30-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="88b30-110">Die Transformation verkleinert das Bild auf 75 × 75 durch Festlegen der horizontalen und vertikalen Skalierungs Werte.</span><span class="sxs-lookup"><span data-stu-id="88b30-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="88b30-111">Im vorherigen Beispiel ist die Bildgröße 75 × 75 und die Ellipse-Größe 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="88b30-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="88b30-112">Da das Bild kleiner als die Ellipse ist, die es füllt, wird die Ellipse mit dem Bild gekachelt.</span><span class="sxs-lookup"><span data-stu-id="88b30-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="88b30-113">Das tiult bedeutet, dass das Bild horizontal und vertikal wiederholt wird, bis die Grenze der Form erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="88b30-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="88b30-114">Weitere Informationen zum Thema tiult finden Sie unter [Tielt a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="88b30-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



