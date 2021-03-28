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
# <a name="clipping-with-a-region"></a><span data-ttu-id="eca76-105">Clipping mit einer Region</span><span class="sxs-lookup"><span data-stu-id="eca76-105">Clipping with a Region</span></span>

<span data-ttu-id="eca76-106">Eine der Eigenschaften der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse ist der Clippingbereich.</span><span class="sxs-lookup"><span data-stu-id="eca76-106">One of the properties of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the clipping region.</span></span> <span data-ttu-id="eca76-107">Alle Zeichnungen, die von einem angegebenen **Grafik** Objekt durchgeführt werden, sind auf den Ausschneide Bereich dieses **Grafik** Objekts beschränkt.</span><span class="sxs-lookup"><span data-stu-id="eca76-107">All drawing done by a given **Graphics** object is restricted to the clipping region of that **Graphics** object.</span></span> <span data-ttu-id="eca76-108">Sie können den Clippingbereich festlegen, indem Sie die **SetClip** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eca76-108">You can set the clipping region by calling the **SetClip** method.</span></span>

<span data-ttu-id="eca76-109">Im folgenden Beispiel wird ein Pfad erstellt, der aus einem einzelnen Polygon besteht.</span><span class="sxs-lookup"><span data-stu-id="eca76-109">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="eca76-110">Anschließend erstellt der Code einen Bereich auf der Grundlage des Pfads.</span><span class="sxs-lookup"><span data-stu-id="eca76-110">Then the code constructs a region based on that path.</span></span> <span data-ttu-id="eca76-111">Die Adresse des Bereichs wird an die **SetClip** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts weitergegeben, und dann werden zwei Zeichen folgen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eca76-111">The address of the region is passed to the **SetClip** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and then two strings are drawn.</span></span>


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



<span data-ttu-id="eca76-112">Die folgende Abbildung zeigt die ausgeschnittenen Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="eca76-112">The following illustration shows the clipped strings.</span></span>

![Abbildung der Teile von zwei Sätzen, die in einer vierseitigen Form angezeigt werden](images/clip1.png)

 

 



