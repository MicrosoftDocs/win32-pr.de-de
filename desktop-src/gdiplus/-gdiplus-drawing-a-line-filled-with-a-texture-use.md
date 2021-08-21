---
description: Anstatt eine Linie oder Kurve mit einer Volltonfarbe zu zeichnen, können Sie mit einer Textur zeichnen.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Zeichnen einer mit einer Textur gefüllten Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467035"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Zeichnen einer mit einer Textur gefüllten Linie

Anstatt eine Linie oder Kurve mit einer Volltonfarbe zu zeichnen, können Sie mit einer Textur zeichnen. Um Linien und Kurven mit einer Textur zu zeichnen, erstellen Sie ein [**TextureBrush-Objekt,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) und übergeben Sie die Adresse dieses **TextureBrush-Objekts** an einen [**Stiftkonstruktor.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Das bild, das dem Texturpinsel zugeordnet ist, wird verwendet, um die Ebene zu kacheln (unsichtbar). Wenn der Stift eine Linie oder Kurve zeichnet, deckt der Strich des Stifts bestimmte Pixel der gekachelten Textur auf.

Im folgenden Beispiel wird ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aus der Datei Texture1.jpg erstellt. Dieses Bild wird verwendet, um ein [**TextureBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) zu erstellen, und das **TextureBrush-Objekt** wird verwendet, um ein [**Stiftobjekt**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) zu erstellen. Der Aufruf von [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) zeichnet das Bild mit der oberen linken Ecke bei (0, 0). Der Aufruf von [**Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) verwendet das **Stiftobjekt,** um eine texturierte Ellipse zu zeichnen.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



Die folgende Abbildung zeigt das Bild und die texturierte Ellipse.

![Abbildung, die ein kleines rechteckiges Bild und dann ein elliptisches Liniensegment zeigt, das mit dem ursprünglichen Bild gefüllt ist](images/pens7.png)

 

 
