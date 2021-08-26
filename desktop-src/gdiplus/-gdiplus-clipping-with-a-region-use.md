---
description: Eine der Eigenschaften der Graphics-Klasse ist der Clippingbereich. Alle Zeichnungen, die von einem bestimmten Grafikobjekt ausgeführt werden, sind auf den Ausschneidebereich dieses Grafikobjekts beschränkt. Sie können den Clippingbereich festlegen, indem Sie die SetClip-Methode aufrufen.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Beschneiden mit einem Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2569350dd0d25066c42fc8ee102cad76e8e77c425bd075122da2179dd3249c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943900"
---
# <a name="clipping-with-a-region"></a>Beschneiden mit einem Bereich

Eine der Eigenschaften der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ist der Clippingbereich. Alle Zeichnungen, die von einem bestimmten **Grafikobjekt** ausgeführt werden, sind auf den Ausschneidebereich dieses **Grafikobjekts** beschränkt. Sie können den Clippingbereich festlegen, indem Sie die **SetClip-Methode** aufrufen.

Im folgenden Beispiel wird ein Pfad erstellt, der aus einem einzelnen Polygon besteht. Anschließend erstellt der Code einen Bereich basierend auf diesem Pfad. Die Adresse des Bereichs wird an die **SetClip-Methode** eines [**Graphics-Objekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben, und dann werden zwei Zeichenfolgen gezeichnet.


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



Die folgende Abbildung zeigt die abgeschnittenen Zeichenfolgen.

![Abbildung, die Teile von zwei Sätzen zeigt, die in einer vierseitigen Form angezeigt werden](images/clip1.png)

 

 



