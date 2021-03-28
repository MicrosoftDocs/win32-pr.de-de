---
description: Eine der Eigenschaften der Grafikklasse ist der Clippingbereich. Alle Zeichnungen, die von einem angegebenen Grafik Objekt durchgeführt werden, sind auf den Ausschneide Bereich dieses Grafik Objekts beschränkt. Sie können den Clippingbereich festlegen, indem Sie die SetClip-Methode aufrufen.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Clipping mit einer Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559495"
---
# <a name="clipping-with-a-region"></a>Clipping mit einer Region

Eine der Eigenschaften der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse ist der Clippingbereich. Alle Zeichnungen, die von einem angegebenen **Grafik** Objekt durchgeführt werden, sind auf den Ausschneide Bereich dieses **Grafik** Objekts beschränkt. Sie können den Clippingbereich festlegen, indem Sie die **SetClip** -Methode aufrufen.

Im folgenden Beispiel wird ein Pfad erstellt, der aus einem einzelnen Polygon besteht. Anschließend erstellt der Code einen Bereich auf der Grundlage des Pfads. Die Adresse des Bereichs wird an die **SetClip** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts weitergegeben, und dann werden zwei Zeichen folgen gezeichnet.


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



Die folgende Abbildung zeigt die ausgeschnittenen Zeichen folgen.

![Abbildung der Teile von zwei Sätzen, die in einer vierseitigen Form angezeigt werden](images/clip1.png)

 

 



