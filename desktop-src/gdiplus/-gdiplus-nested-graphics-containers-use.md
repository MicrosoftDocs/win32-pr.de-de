---
description: Windows GDI+ stellt Container bereit, die Sie verwenden können, um einen Teil des Zustands in einem Grafik Objekt temporär zu ersetzen oder zu erweitern.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Geschachtelte Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959450"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="10118-103">Geschachtelte Grafikcontainer</span><span class="sxs-lookup"><span data-stu-id="10118-103">Nested Graphics Containers</span></span>

<span data-ttu-id="10118-104">Windows GDI+ stellt Container bereit, die Sie verwenden können, um einen Teil des Zustands in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt temporär zu ersetzen oder zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="10118-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="10118-105">Sie erstellen einen Container durch Aufrufen der [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) -Methode eines **Grafik** Objekts.</span><span class="sxs-lookup"><span data-stu-id="10118-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="10118-106">Sie können " **Graphics:: BeginContainer** " wiederholt aufrufen, um in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10118-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="10118-107">Transformationen in der Liste der Container</span><span class="sxs-lookup"><span data-stu-id="10118-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="10118-108">Im folgenden Beispiel werden ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein Container innerhalb dieses **Grafik** Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="10118-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="10118-109">Die globale Transformation des **Grafik** Objekts ist eine Translation 100-Einheiten in der x-Richtung und 80-Einheiten in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="10118-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="10118-110">Die Welt Transformation des Containers ist eine 30-Grad-Rotation.</span><span class="sxs-lookup"><span data-stu-id="10118-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="10118-111">Der Code führt den-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="10118-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="10118-112">zweimal.</span><span class="sxs-lookup"><span data-stu-id="10118-112">twice.</span></span> <span data-ttu-id="10118-113">Der erste Grafik Befehl [**::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) befindet sich *innerhalb des Containers*. Das heißt, der Aufruf erfolgt zwischen den Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="10118-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="10118-114">Der zweite aufzurufende **Grafik::D rawrechteck** ist nach dem aufzurufenden **Grafik:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="10118-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="10118-115">Im vorangehenden Code wird das aus dem Container gezogene Rechteck zuerst von der Welt Transformation des Containers (Drehung) und dann von der Welt Transformation des [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts (Translation) transformiert.</span><span class="sxs-lookup"><span data-stu-id="10118-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="10118-116">Das von außerhalb des Containers gezeichnete Rechteck wird nur durch die Welt Transformation des **Grafik** Objekts (Translation) transformiert.</span><span class="sxs-lookup"><span data-stu-id="10118-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="10118-117">Die folgende Abbildung zeigt die beiden Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="10118-117">The following illustration shows the two rectangles.</span></span>

![Screenshot eines Fensters mit zwei roten Rechtecke, die denselben Punkt zentriert haben, aber mit unterschiedlichen Drehungen](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="10118-119">Clipping in geschbten Containern</span><span class="sxs-lookup"><span data-stu-id="10118-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="10118-120">Im folgenden Beispiel wird veranschaulicht, wie die geschbten Container Clippingbereiche verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="10118-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="10118-121">Der Code erstellt ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und einen Container in diesem **Grafik** Objekt.</span><span class="sxs-lookup"><span data-stu-id="10118-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="10118-122">Der Clippingbereich des **Grafik** Objekts ist ein Rechteck, und der Clippingbereich des Containers ist eine Ellipse.</span><span class="sxs-lookup"><span data-stu-id="10118-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="10118-123">Der Code führt zwei Aufrufe an die [**Grafiken aus::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="10118-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="10118-124">Der erste Grafik Befehl **::D rawline** befindet sich innerhalb des Containers, und der zweite aufzurufende **Grafik::D rawline** befindet sich außerhalb des Containers (nach dem aufzurufen von [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="10118-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="10118-125">Die erste Zeile wird durch die Schnittmenge der beiden Clippingbereiche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10118-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="10118-126">Die zweite Zeile wird nur durch den rechteckigen Clippingbereich des **Grafik** Objekts abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10118-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="10118-127">Die folgende Abbildung zeigt die beiden ausgeschnittenen Zeilen.</span><span class="sxs-lookup"><span data-stu-id="10118-127">The following illustration shows the two clipped lines.</span></span>

![Abbildung einer Ellipse innerhalb eines Rechtecks, bei der eine Zeile von der Ellipse und die andere durch das Rechteck abgeschnitten wurde](images/nestedcontainers2.png)

<span data-ttu-id="10118-129">Wie die beiden vorherigen Beispiele zeigen, sind Transformationen und Clippingbereiche in geschposteten Containern kumulativ.</span><span class="sxs-lookup"><span data-stu-id="10118-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="10118-130">Wenn Sie die globalen Transformationen für den Container und das [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt festlegen, gelten beide Transformationen für Elemente, die aus dem Container gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="10118-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="10118-131">Die Transformation des Containers wird zuerst angewendet, und die Transformation des **Grafik** Objekts wird als zweites angewendet.</span><span class="sxs-lookup"><span data-stu-id="10118-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="10118-132">Wenn Sie die Ausschneide Bereiche des Containers und des **Grafik** Objekts festlegen, werden die Elemente, die aus dem Container gezogen werden, durch die Schnittmenge der beiden Clippingbereiche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10118-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="10118-133">Qualitätseinstellungen in der Liste der Container</span><span class="sxs-lookup"><span data-stu-id="10118-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="10118-134">Qualitätseinstellungen (" [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)", " [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)" und "like") in den nativen Containern sind nicht kumulativ. Stattdessen ersetzen die Qualitätseinstellungen des Containers vorübergehend die Qualitätseinstellungen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.</span><span class="sxs-lookup"><span data-stu-id="10118-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="10118-135">Wenn Sie einen neuen Container erstellen, werden die Qualitätseinstellungen für diesen Container auf Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10118-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="10118-136">Nehmen Sie beispielsweise an, Sie verfügen über ein **Grafik** Objekt mit dem Glättungs Modus [\* \* \* \* SmoothingModeAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span><span class="sxs-lookup"><span data-stu-id="10118-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="10118-137">Wenn Sie einen Container erstellen, ist der Glättungs Modus innerhalb des Containers der standardmäßige Glättungs Modus.</span><span class="sxs-lookup"><span data-stu-id="10118-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="10118-138">Sie können den Glättungs Modus des Containers festlegen, und alle Elemente, die aus dem Container gezogen werden, werden gemäß dem von Ihnen festgelegten Modus gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10118-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="10118-139">Elemente, die nach dem Aufrufen von [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) gezeichnet werden, werden gemäß dem Glättungs Modus ([\* \* \* \* SmoothingModeAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) gezeichnet, der vor dem Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="10118-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="10118-140">Mehrere Ebenen von als Container</span><span class="sxs-lookup"><span data-stu-id="10118-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="10118-141">Sie sind nicht auf einen Container in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt beschränkt.</span><span class="sxs-lookup"><span data-stu-id="10118-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="10118-142">Sie können eine Reihe von Containern erstellen, die jeweils in der vorherigen geschpotet sind, und Sie können die Welt Transformation, den Clippingbereich und die Qualitätseinstellungen der einzelnen geschposteten Container angeben.</span><span class="sxs-lookup"><span data-stu-id="10118-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="10118-143">Wenn Sie eine Zeichnungs Methode aus dem innersten Container heraus aufzurufen, werden die Transformationen in der richtigen Reihenfolge angewendet, beginnend mit dem innersten Container und enden mit dem äußersten Container.</span><span class="sxs-lookup"><span data-stu-id="10118-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="10118-144">Elemente, die aus dem innersten Container gezeichnet werden, werden durch die Schnittmenge aller Clippingbereiche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10118-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="10118-145">Im folgenden Beispiel wird ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt und der Text Rendering-Hinweis auf [\* \* \* \* textrenderinghintantialias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10118-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="10118-146">Der Code erstellt zwei Container, von denen eine geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="10118-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="10118-147">Der Text Rendering-Hinweis des äußeren Containers ist auf [\* \* \* \* TextRenderingHintSingleBitPerPixel \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \* festgelegt, und der Text Rendering-Hinweis des inneren Containers ist auf [\* \* \* \* textrenderinghintantialias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10118-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="10118-148">Der Code zeichnet drei Zeichen folgen: eine aus dem inneren Container, eine aus dem äußeren Container und eine aus dem **Grafik** Objekt selbst.</span><span class="sxs-lookup"><span data-stu-id="10118-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="10118-149">Die folgende Abbildung zeigt die drei Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="10118-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="10118-150">Die Zeichen folgen, die aus dem inneren Container und dem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gezeichnet werden, werden durch Antialiasing geglättet.</span><span class="sxs-lookup"><span data-stu-id="10118-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="10118-151">Die aus dem äußeren Container gezeichnete Zeichenfolge wird aufgrund der TextRenderingHintSingleBitPerPixel-Einstellung nicht durch Antialiasing geglättet.</span><span class="sxs-lookup"><span data-stu-id="10118-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![Abbildung eines Rechtecks, das die gleiche Zeichenfolge enthält. nur die Zeichen in der ersten und letzten Zeile sind glatt.](images/nestedcontainers3.png)

 

 
