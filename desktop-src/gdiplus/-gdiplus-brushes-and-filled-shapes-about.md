---
description: Eine geschlossene Abbildung, wie z. b. ein Rechteck oder eine Ellipse, besteht aus einem Umriss und einem inneren.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinsel und gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567247"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="79037-103">Pinsel und gefüllte Formen</span><span class="sxs-lookup"><span data-stu-id="79037-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="79037-104">Eine geschlossene Abbildung, wie z. b. ein Rechteck oder eine Ellipse, besteht aus einem Umriss und einem inneren.</span><span class="sxs-lookup"><span data-stu-id="79037-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="79037-105">Die Gliederung wird mit einem [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekt gezeichnet, und das Innere ist mit einem [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt gefüllt.</span><span class="sxs-lookup"><span data-stu-id="79037-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="79037-106">Windows GDI+ bietet verschiedene Pinsel Klassen zum Auffüllen des Inneren von geschlossenen Abbildungen: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)und [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="79037-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="79037-107">Alle diese Klassen erben von der **Brush** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="79037-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="79037-108">Die folgende Abbildung zeigt ein Rechteck, das mit einem Pinsel gefüllt ist, und eine Ellipse mit einem Schraffurpinsel.</span><span class="sxs-lookup"><span data-stu-id="79037-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![Darstellung eines blauen Rechtecks und einer Magenta-Ellipse mit einem blauen Schraffurmuster](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="79037-110">Vollpinsel</span><span class="sxs-lookup"><span data-stu-id="79037-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="79037-111">Pinsel Schraffur</span><span class="sxs-lookup"><span data-stu-id="79037-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="79037-112">Textur Pinsel</span><span class="sxs-lookup"><span data-stu-id="79037-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="79037-113">Farbverlaufs Pinsel</span><span class="sxs-lookup"><span data-stu-id="79037-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="79037-114">Vollpinsel</span><span class="sxs-lookup"><span data-stu-id="79037-114">Solid Brushes</span></span>

<span data-ttu-id="79037-115">Um eine geschlossene Form auszufüllen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="79037-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="79037-116">Das **graphics** -Objekt stellt Methoden bereit, z. b. [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) und [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), und das **Brush** -Objekt speichert Attribute der Füllung, z. b. Farbe und Muster.</span><span class="sxs-lookup"><span data-stu-id="79037-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="79037-117">Die Adresse des **Pinsel** Objekts wird als eines der Argumente an die Fill-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="79037-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="79037-118">Im folgenden Beispiel wird eine Ellipse mit einer roten Farbe gefüllt.</span><span class="sxs-lookup"><span data-stu-id="79037-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="79037-119">Beachten Sie, dass im vorherigen Beispiel der Pinsel den Typ [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)hat, der von [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)erbt.</span><span class="sxs-lookup"><span data-stu-id="79037-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="79037-120">Pinsel Schraffur</span><span class="sxs-lookup"><span data-stu-id="79037-120">Hatch Brushes</span></span>

<span data-ttu-id="79037-121">Wenn Sie eine Form mit einem Schraffurpinsel ausfüllen, geben Sie eine Vordergrundfarbe, eine Hintergrundfarbe und eine Schraffurart an.</span><span class="sxs-lookup"><span data-stu-id="79037-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="79037-122">Die Vordergrundfarbe ist die Farbe der Schraffur.</span><span class="sxs-lookup"><span data-stu-id="79037-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="79037-123">GDI+ bietet mehr als 50 Schraffurstile, die in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="79037-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="79037-124">Die drei in der folgenden Abbildung gezeigten Stile sind horizontal, ForwardDiagonal und Cross.</span><span class="sxs-lookup"><span data-stu-id="79037-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![Abbildung, die drei Teal-farbige Ellipsen anzeigt, die jeweils eine andere Schraffurart haben](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="79037-126">Textur Pinsel</span><span class="sxs-lookup"><span data-stu-id="79037-126">Texture Brushes</span></span>

<span data-ttu-id="79037-127">Mit einem Textur Pinsel können Sie eine Form mit einem Muster ausfüllen, das in einer Bitmap gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="79037-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="79037-128">Angenommen, das folgende Bild ist in einer Datenträger Datei mit dem Namen MyTexture.bmp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79037-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![Screenshot eines kleinen Quadrats, das mit verschiedenen Farben gefüllt ist](images/aboutgdip02-art19.png)

<span data-ttu-id="79037-130&quot;>Im folgenden Beispiel wird eine Ellipse gefüllt, indem das in MyTexture.bmp gespeicherte Bild wiederholt wird.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;79037-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="79037-131">Die folgende Abbildung zeigt die gefüllte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="79037-131">The following illustration shows the filled ellipse.</span></span>

![Abbildung, die eine mit dem zuvor definierten Muster Gefüllte Ellipse anzeigt](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="79037-133">Farbverlaufs Pinsel</span><span class="sxs-lookup"><span data-stu-id="79037-133">Gradient Brushes</span></span>

<span data-ttu-id="79037-134">Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer Farbe auszufüllen, die sich allmählich von einem Teil der Form in einen anderen ändert.</span><span class="sxs-lookup"><span data-stu-id="79037-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="79037-135">Ein horizontaler Farbverlaufs Pinsel ändert z. b. die Farbe, wenn Sie von der linken Seite der Abbildung auf die Rechte Seite wechseln.</span><span class="sxs-lookup"><span data-stu-id="79037-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="79037-136">Im folgenden Beispiel wird eine Ellipse mit einem horizontalen Farbverlaufs Pinsel gefüllt, der sich von blau in grün ändert, wenn Sie von der linken Seite der Ellipse auf die Rechte Seite wechseln.</span><span class="sxs-lookup"><span data-stu-id="79037-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="79037-137">Die folgende Abbildung zeigt die gefüllte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="79037-137">The following illustration shows the filled ellipse.</span></span>

![Abbildung, die eine Ellipse mit einem Farbverlaufs Füll Diagramm anzeigt, rechts nach grün Links](images/aboutgdip02-art21.png)

<span data-ttu-id="79037-139">Ein Pinsel mit dem Pfad Farbverlauf kann so konfiguriert werden, dass die Farbe geändert wird, wenn Sie von der Mitte einer Abbildung zur Grenze wechseln.</span><span class="sxs-lookup"><span data-stu-id="79037-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![Ilustration einer Ellipse, die im Mittelpunkt dunkelblau ist, Schattierung auf hellblau am Rand](images/aboutgdip02-art22.png)

<span data-ttu-id="79037-141">Pfad Farbverlaufs Pinsel sind recht flexibel.</span><span class="sxs-lookup"><span data-stu-id="79037-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="79037-142">Der Farbverlaufs Pinsel, der zum Ausfüllen des Dreiecks in der folgenden Abbildung verwendet wird, ändert sich allmählich von rot in der Mitte zu jeder der drei verschiedenen Farben in den Scheitel Punkten.</span><span class="sxs-lookup"><span data-stu-id="79037-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![Abbildung eines Dreiecks, das in der Mitte rot ist, und Schattierung in eine andere Farbe an jedem Scheitelpunkt](images/aboutgdip02-art23.png)

 

 



