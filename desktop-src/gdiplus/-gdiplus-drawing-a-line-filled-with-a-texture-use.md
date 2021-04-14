---
description: Anstatt eine Linie oder Kurve mit einer voll Tonfarbe zu zeichnen, können Sie mit einer Textur zeichnen.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Zeichnen einer mit einer Textur ausgefüllten Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979049"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Zeichnen einer mit einer Textur ausgefüllten Linie

Anstatt eine Linie oder Kurve mit einer voll Tonfarbe zu zeichnen, können Sie mit einer Textur zeichnen. Um Linien und Kurven mit einer Textur zu zeichnen, erstellen Sie ein [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekt, und übergeben Sie die Adresse des **TextureBrush** -Objekts an einen [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor. Das Bild, das dem Textur Pinsel zugeordnet ist, wird verwendet, um die Ebene (unsichtbar) zu Kacheln, und wenn der Stift eine Linie oder Kurve zeichnet, wird der Strich des Stifts bestimmte Pixel der Kachel Textur nicht abdecken.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei Texture1.jpg erstellt. Dieses Bild wird verwendet, um ein [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) -Objekt zu erstellen, und das **TextureBrush** -Objekt wird verwendet, um ein [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Objekt zu erstellen. Der Bild- [**:D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) zeichnet das Bild mit seiner oberen linken Ecke bei (0,0). Beim Aufrufen von [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) wird das **Pen** -Objekt verwendet, um eine strukturierte Ellipse zu zeichnen.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



Die folgende Abbildung zeigt das Bild und die strukturierte Ellipse.

![Abbildung zeigt ein kleines rechteckiges Bild, ein elliptisches Liniensegment, das mit dem ursprünglichen Bild gefüllt ist](images/pens7.png)

 

 
