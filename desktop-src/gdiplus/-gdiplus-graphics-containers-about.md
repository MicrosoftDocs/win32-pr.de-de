---
description: Grafik Zustand &\# 8212; Clippingbereich, Transformationen und Qualitätseinstellungen &\# 8212; wird in einem Grafik Objekt gespeichert.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570857"
---
# <a name="graphics-containers"></a><span data-ttu-id="9723b-103">Grafikcontainer</span><span class="sxs-lookup"><span data-stu-id="9723b-103">Graphics Containers</span></span>

<span data-ttu-id="9723b-104">Grafik Zustand – Clippingbereich, Transformationen und Qualitätseinstellungen – wird in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9723b-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="9723b-105">Windows GDI+ ermöglicht es Ihnen, einen Teil des Zustands in einem **Grafik** Objekt mithilfe eines Containers temporär zu ersetzen oder zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9723b-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="9723b-106">Sie starten einen Container durch Aufrufen der [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) -Methode eines **Grafik** Objekts und Beenden einen Container durch Aufrufen der [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9723b-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="9723b-107">Zwischen **Grafiken:: BeginContainer** und **Graphics:: EndContainer** gehören alle Zustandsänderungen, die Sie am **Grafik** Objekt vornehmen, zum Container und überschreiben den vorhandenen Zustand des **Grafik** Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="9723b-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="9723b-108">Im folgenden Beispiel wird ein Container in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9723b-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="9723b-109">Die globale Transformation des **Grafik** Objekts ist eine Übersetzung von 200 Einheiten auf der rechten Seite, und die weltweite Transformation des Containers ist eine Übersetzung von 100 Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9723b-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="9723b-110">Beachten Sie, dass im vorherigen Beispiel die-Anweisung `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` zwischen den Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) ein anderes Rechteck erzeugt als dieselbe Anweisung, die nach dem Aufruf von **Graphics:: EndContainer** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9723b-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="9723b-111">Nur die horizontale Übersetzung gilt für den **drawrechteck** -Befehl, der außerhalb des Containers erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9723b-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="9723b-112">Beide Transformationen – die horizontale Übersetzung von 200 Einheiten und die vertikale Übersetzung von 100 Einheiten – gelten für die [**Grafiken::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Aufrufe innerhalb des Containers.</span><span class="sxs-lookup"><span data-stu-id="9723b-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="9723b-113">Die folgende Abbildung zeigt die beiden Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="9723b-113">The following illustration shows the two rectangles.</span></span>

![Screenshot eines Fensters mit zwei Rechtecke, die mit einem blauen Stift gezeichnet werden, einer mit der anderen Position](images/aboutgdip05-art17.png)

<span data-ttu-id="9723b-115">Container können in Containern geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="9723b-115">Containers can be nested within containers.</span></span> <span data-ttu-id="9723b-116">Im folgenden Beispiel wird ein Container innerhalb eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und ein anderer Container innerhalb des ersten Containers erstellt.</span><span class="sxs-lookup"><span data-stu-id="9723b-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="9723b-117">Die globale Transformation des **Grafik** Objekts ist eine Translation 100-Einheiten in der x-Richtung und 80-Einheiten in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="9723b-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="9723b-118">Die Welt Transformation des ersten Containers ist eine 30-Grad-Rotation.</span><span class="sxs-lookup"><span data-stu-id="9723b-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="9723b-119">Die globale Transformation des zweiten Containers ist eine Skalierung mit einem Faktor von 2 in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="9723b-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="9723b-120">Ein aufzurufende [**Grafik::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) -Methode wird innerhalb des zweiten Containers erstellt.</span><span class="sxs-lookup"><span data-stu-id="9723b-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="9723b-121">Die folgende Abbildung zeigt die Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9723b-121">The following illustration shows the ellipse.</span></span>

![Screenshot eines Fensters, das eine gedrehte blaue Ellipse enthält, deren Mitte als (100, 80) bezeichnet wird](images/aboutgdip05-art18.png)

<span data-ttu-id="9723b-123">Beachten Sie, dass alle drei Transformationen auf die [**Grafiken zutreffen::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) -Aufrufe im zweiten Container (innersten).</span><span class="sxs-lookup"><span data-stu-id="9723b-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="9723b-124">Beachten Sie auch die Reihenfolge der Transformationen: erste Skalierung, dann drehen und dann übersetzen.</span><span class="sxs-lookup"><span data-stu-id="9723b-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="9723b-125">Die innerste Transformation wird zuerst angewendet, und die äußerste Transformation wird zuletzt angewendet.</span><span class="sxs-lookup"><span data-stu-id="9723b-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="9723b-126">Jede Eigenschaft eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts kann innerhalb eines Containers (zwischen den Aufrufen von [**Grafiken:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9723b-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="9723b-127">Beispielsweise kann ein Clippingbereich innerhalb eines Containers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9723b-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="9723b-128">Jede im Container ausgeführte Zeichnung wird auf den Ausschneide Bereich dieses Containers beschränkt und wird auch auf die Ausschneide Bereiche beliebiger äußerer Container und den Ausschneide Bereich des **Grafik** Objekts beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9723b-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="9723b-129">Die bisher erörterten Eigenschaften – die globale Transformation und der Clippingbereich – werden durch die Kombination aus den vorschangen Containern kombiniert.</span><span class="sxs-lookup"><span data-stu-id="9723b-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="9723b-130">Andere Eigenschaften werden vorübergehend durch einen in einem Container ausgefallenen Container ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9723b-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="9723b-131">Wenn Sie z. b. den Glättungs Modus in einem Container auf "SmoothingModeAntiAlias" festlegen, verwenden alle in diesem Container aufgerufenen Zeichnungs Methoden den AntiAlias-Glättungs Modus, aber Zeichnungs Methoden, die nach " [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) " aufgerufen werden, verwenden den Glättungs Modus, der vor dem Aufruf von " [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))"</span><span class="sxs-lookup"><span data-stu-id="9723b-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="9723b-132">Ein weiteres Beispiel für die Kombination der weltweiten Transformationen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und eines Containers ist, dass Sie einen Augenblick zeichnen und an verschiedenen Positionen in einer Sequenz von Flächen platzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9723b-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="9723b-133">Im folgenden Beispiel wird ein Auge gezeichnet, der sich am Ursprung des Koordinatensystems zentriert.</span><span class="sxs-lookup"><span data-stu-id="9723b-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="9723b-134">In der folgenden Abbildung sind die Augen-und Koordinatenachsen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9723b-134">The following illustration shows the eye and the coordinate axes.</span></span>

![Darstellung eines Auges, das aus drei Ellipsen besteht: jeweils eine für die Kontur, Iris und Schülerin](images/aboutgdip05-art19.png)

<span data-ttu-id="9723b-136">Die im vorherigen Beispiel definierte DrawEye-Funktion empfängt die Adresse eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und erstellt sofort einen Container in diesem **Grafik** Objekt.</span><span class="sxs-lookup"><span data-stu-id="9723b-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="9723b-137">Dieser Container isoliert jeden Code, der die DrawEye-Funktion aus den Eigenschafts Einstellungen aufruft, die während der Ausführung der DrawEye-Funktion erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9723b-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="9723b-138">Beispielsweise legt der Code in der DrawEye-Funktion den Ausschneide Bereich des **Grafik** Objekts fest. wenn DrawEye jedoch die Steuerung an die aufrufende Routine zurückgibt, ist der Clippingbereich so, wie er vor dem Aufruf von DrawEye war.</span><span class="sxs-lookup"><span data-stu-id="9723b-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="9723b-139">Im folgenden Beispiel werden drei Ellipsen (Gesichter) gezeichnet, die jeweils einen Augenblick innerhalb von haben.</span><span class="sxs-lookup"><span data-stu-id="9723b-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="9723b-140">Die folgende Abbildung zeigt die drei Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="9723b-140">The following illustration shows the three ellipses.</span></span>

![Screenshot eines Fensters mit drei Ellipsen, von denen jedes ein Auge auf eine andere Größe und Drehung enthält](images/aboutgdip05-art20.png)

<span data-ttu-id="9723b-142">Im vorherigen Beispiel werden alle Ellipsen mit dem-Befehl gezeichnet `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , der eine Ellipse zeichnet, die sich am Ursprung des Koordinatensystems zentriert.</span><span class="sxs-lookup"><span data-stu-id="9723b-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="9723b-143">Die Ellipsen werden von der oberen linken Ecke des Client Bereichs durch Festlegen der Welt Transformation des [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts entfernt.</span><span class="sxs-lookup"><span data-stu-id="9723b-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="9723b-144">Die-Anweisung bewirkt, dass die erste Ellipse um (100, 100) zentriert wird.</span><span class="sxs-lookup"><span data-stu-id="9723b-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="9723b-145">Die-Anweisung bewirkt, dass der Mittelpunkt der zweiten Ellipse 100 Einheiten rechts neben der Mitte der ersten Ellipse ist.</span><span class="sxs-lookup"><span data-stu-id="9723b-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="9723b-146">Ebenso ist der Mittelpunkt der dritten Ellipse 100 Einheiten rechts neben der Mitte der zweiten Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9723b-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="9723b-147">Mithilfe der Container im vorherigen Beispiel wird das Auge relativ zum Mittelpunkt einer bestimmten Ellipse transformiert.</span><span class="sxs-lookup"><span data-stu-id="9723b-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="9723b-148">Das erste Auge wird in der Mitte der Ellipse ohne Transformation gezeichnet, sodass sich der DrawEye-Befehl nicht in einem Container befindet.</span><span class="sxs-lookup"><span data-stu-id="9723b-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="9723b-149">Das zweite Auge wird um 40 Grad gedreht und 30 Einheiten über dem Mittelpunkt der Ellipse gezeichnet, sodass die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9723b-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="9723b-150">Das dritte Auge wird gestreckt, gedreht und in der Mitte der Ellipse gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9723b-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="9723b-151">Wie beim zweiten Blick werden die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9723b-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
