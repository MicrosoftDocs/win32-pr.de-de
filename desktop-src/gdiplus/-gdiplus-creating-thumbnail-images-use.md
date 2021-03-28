---
description: Bei einem Miniaturbild handelt es sich um eine kleine Version eines Bilds. Sie können ein Miniaturbild erstellen, indem Sie die GetThumbnailImage-Methode eines Bildobjekts aufrufen.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Erstellen von Miniaturbildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565820"
---
# <a name="creating-thumbnail-images"></a><span data-ttu-id="3d002-104">Erstellen von Miniaturbildern</span><span class="sxs-lookup"><span data-stu-id="3d002-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="3d002-105">Bei einem Miniaturbild handelt es sich um eine kleine Version eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="3d002-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="3d002-106">Sie können ein Miniaturbild erstellen, indem Sie die **GetThumbnailImage** -Methode eines [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3d002-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="3d002-107">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei Compass.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d002-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="3d002-108">Das ursprüngliche Bild hat eine Breite von 640 Pixeln und eine Höhe von 479 Pixel.</span><span class="sxs-lookup"><span data-stu-id="3d002-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="3d002-109">Der Code erstellt ein Miniaturbild mit einer Breite von 100 Pixeln und einer Höhe von 100 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="3d002-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="3d002-110">In der folgenden Abbildung ist das Miniaturbild dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3d002-110">The following illustration shows the thumbnail image.</span></span>

![Abbildung einer kleinen Grafik, die einen Kompass anzeigt](images/thumbnail1.png)

 

 



