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
# <a name="filling-a-shape-with-an-image-texture"></a>Auffüllen einer Form mit einer Bildstruktur

Sie können eine geschlossene Form mit einer Textur auffüllen, indem Sie die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse und die [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Klasse verwenden.

Im folgenden Beispiel wird eine Ellipse mit einem Bild gefüllt. Der Code erstellt ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und übergibt dann die Adresse dieses **Bild** Objekts als Argument an einen [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Konstruktor. Die dritte Code Anweisung skaliert das Bild, und die vierte Anweisung füllt die Ellipse mit wiederholten Kopien des skalierten Bilds:


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



Im vorangehenden Codebeispiel legt die [**TextureBrush:: setTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) -Methode die Transformation fest, die auf das Bild angewendet wird, bevor Sie gezeichnet wird. Angenommen, das ursprüngliche Bild hat eine Breite von 640 Pixeln und eine Höhe von 480 Pixel. Die Transformation verkleinert das Bild auf 75 × 75 durch Festlegen der horizontalen und vertikalen Skalierungs Werte.

> [!Note]  
> Im vorherigen Beispiel ist die Bildgröße 75 × 75 und die Ellipse-Größe 150 × 250. Da das Bild kleiner als die Ellipse ist, die es füllt, wird die Ellipse mit dem Bild gekachelt. Das tiult bedeutet, dass das Bild horizontal und vertikal wiederholt wird, bis die Grenze der Form erreicht ist. Weitere Informationen zum Thema tiult finden Sie unter [Tielt a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



