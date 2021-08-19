---
description: Ein Miniaturbild ist eine kleine Version eines Bilds. Sie können ein Miniaturbild erstellen, indem Sie die GetThumbnailImage-Methode eines Image-Objekts aufrufen.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Erstellen von Miniaturbildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d44fec3220bef7a6691d3852d16f90e9cf43635c99f69bba16f3b569ebabc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696311"
---
# <a name="creating-thumbnail-images"></a>Erstellen von Miniaturbildern

Ein Miniaturbild ist eine kleine Version eines Bilds. Sie können ein Miniaturbild erstellen, indem Sie die **GetThumbnailImage-Methode** eines [**Image-Objekts**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen.

Im folgenden Beispiel wird ein [**Image-Objekt aus**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) der Datei Compass.bmp. Das ursprüngliche Bild hat eine Breite von 640 Pixel und eine Höhe von 479 Pixeln. Der Code erstellt ein Miniaturbild mit einer Breite von 100 Pixeln und einer Höhe von 100 Pixeln.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



Die folgende Abbildung zeigt das Miniaturbild.

![Abbildung einer kleinen Grafik, die einen Kompass zeigt](images/thumbnail1.png)

 

 



