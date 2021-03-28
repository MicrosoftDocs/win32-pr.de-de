---
description: Wenn Sie nur die linke obere Ecke eines Bilds an die DrawImage-Methode übergeben, kann Windows GDI+ das Image skalieren, wodurch die Leistung beeinträchtigt wird.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Verbessern der Leistung durch vermeiden der automatischen Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979008"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="571c4-103">Verbessern der Leistung durch vermeiden der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="571c4-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="571c4-104">Wenn Sie nur die linke obere Ecke eines Bilds an die **DrawImage** -Methode übergeben, kann Windows GDI+ das Image skalieren, wodurch die Leistung beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="571c4-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="571c4-105">Der folgende Rückruf der **DrawImage** -Methode gibt eine linke obere Ecke von (50, 30) an, gibt jedoch kein Ziel Rechteck an:</span><span class="sxs-lookup"><span data-stu-id="571c4-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="571c4-106">Obwohl es sich hierbei um die einfachste Version der **DrawImage** -Methode im Hinblick auf die Anzahl der erforderlichen Argumente handelt, ist dies nicht unbedingt die effizienteste Methode.</span><span class="sxs-lookup"><span data-stu-id="571c4-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="571c4-107">Wenn sich die Anzahl der Punkte pro Zoll auf dem aktuellen Anzeigegerät von der Anzahl der Punkte pro Zoll auf dem Gerät unterscheidet, auf dem das Abbild erstellt wurde, skaliert GDI+ das Abbild so, dass seine physische Größe auf dem aktuellen Anzeigegerät so nah wie möglich auf dem Gerät ist, auf dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="571c4-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="571c4-108">Wenn Sie eine solche Skalierung vermeiden möchten, übergeben Sie die Breite und Höhe eines Ziel Rechtecks an die **DrawImage** -Methode.</span><span class="sxs-lookup"><span data-stu-id="571c4-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="571c4-109">Im folgenden Beispiel wird das gleiche Bild zweimal gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="571c4-109">The following example draws the same image twice.</span></span> <span data-ttu-id="571c4-110">Im ersten Fall werden die Breite und Höhe des Ziel Rechtecks nicht angegeben, und das Bild wird automatisch skaliert.</span><span class="sxs-lookup"><span data-stu-id="571c4-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="571c4-111">Im zweiten Fall werden Breite und Höhe (gemessen in Pixel) des Ziel Rechtecks als identisch mit der Breite und Höhe des ursprünglichen Bilds angegeben.</span><span class="sxs-lookup"><span data-stu-id="571c4-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="571c4-112">In der folgenden Abbildung wird das Bild zweimal gerendert.</span><span class="sxs-lookup"><span data-stu-id="571c4-112">The following illustration shows the image rendered twice.</span></span>

![Screenshot eines Fensters, das zwei Versionen eines Bilds in unterschiedlichen Skalen enthält](images/scaledtexture1.png)

 

 



