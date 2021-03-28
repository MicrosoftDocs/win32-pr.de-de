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
# <a name="creating-thumbnail-images"></a>Erstellen von Miniaturbildern

Bei einem Miniaturbild handelt es sich um eine kleine Version eines Bilds. Sie können ein Miniaturbild erstellen, indem Sie die **GetThumbnailImage** -Methode eines [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts aufrufen.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei Compass.bmp erstellt. Das ursprüngliche Bild hat eine Breite von 640 Pixeln und eine Höhe von 479 Pixel. Der Code erstellt ein Miniaturbild mit einer Breite von 100 Pixeln und einer Höhe von 100 Pixeln.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



In der folgenden Abbildung ist das Miniaturbild dargestellt.

![Abbildung einer kleinen Grafik, die einen Kompass anzeigt](images/thumbnail1.png)

 

 



