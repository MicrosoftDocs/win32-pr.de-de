---
description: Um eine Form mit einer voll Tonfarbe auszufüllen, erstellen Sie ein SolidBrush-Objekt, und übergeben Sie dann die Adresse des SolidBrush-Objekts als Argument an eine der Füll Methoden der Grafikklasse.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Auffüllen einer Form mit einer voll Tonfarbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994262"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="00bd3-103">Auffüllen einer Form mit einer voll Tonfarbe</span><span class="sxs-lookup"><span data-stu-id="00bd3-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="00bd3-104">Um eine Form mit einer voll Tonfarbe auszufüllen, erstellen Sie ein [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekt, und übergeben Sie dann die Adresse des **SolidBrush** -Objekts als Argument an eine der Füll Methoden der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse.</span><span class="sxs-lookup"><span data-stu-id="00bd3-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="00bd3-105">Im folgenden Beispiel wird gezeigt, wie eine Ellipse mit der Farbe Rot aufgefüllt wird:</span><span class="sxs-lookup"><span data-stu-id="00bd3-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="00bd3-106">Im vorherigen Beispiel nimmt der [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Konstruktor einen [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) -Objekt Verweis als einziges Argument an.</span><span class="sxs-lookup"><span data-stu-id="00bd3-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="00bd3-107">Die Werte, die vom **farbkonstruktor** verwendet werden, stellen die Alpha-, rot-, grün-und Blau-Komponenten der Farbe dar.</span><span class="sxs-lookup"><span data-stu-id="00bd3-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="00bd3-108">Jeder dieser Werte muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="00bd3-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="00bd3-109">Der erste 255 gibt an, dass die Farbe vollständig undurchsichtig ist, und der zweite 255 gibt an, dass die rote Komponente vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="00bd3-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="00bd3-110">Die beiden Nullen zeigen an, dass die grünen und blauen Komponenten beide eine Intensität von 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="00bd3-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="00bd3-111">Die vier Zahlen (0, 0, 100, 60), die an die [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) -Methode übergeben werden, geben den Speicherort und die Größe des umschließenden Rechtecks für die Ellipse an.</span><span class="sxs-lookup"><span data-stu-id="00bd3-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="00bd3-112">Das Rechteck hat eine linke obere Ecke von (0,0), eine Breite von 100 und eine Höhe von 60.</span><span class="sxs-lookup"><span data-stu-id="00bd3-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
