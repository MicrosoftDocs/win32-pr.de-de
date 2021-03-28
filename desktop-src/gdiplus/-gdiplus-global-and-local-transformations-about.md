---
description: Eine globale Transformation ist eine Transformation, die auf jedes Element angewendet wird, das von einem angegebenen Grafik Objekt gezeichnet wird.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Globale und lokale Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551226"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="efd40-103">Globale und lokale Transformationen</span><span class="sxs-lookup"><span data-stu-id="efd40-103">Global and Local Transformations</span></span>

<span data-ttu-id="efd40-104">Eine globale Transformation ist eine Transformation, die auf jedes Element angewendet wird, das von einem angegebenen [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="efd40-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="efd40-105">Um eine globale Transformation zu erstellen, erstellen Sie ein **Grafik** Objekt, und rufen Sie dann die zugehörige [**Graphics:: setTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="efd40-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="efd40-106">Die **Graphics:: setTransform** -Methode manipuliert ein [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt, das dem **Grafik** Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="efd40-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="efd40-107">Die in diesem **Matrix** Objekt gespeicherte Transformation wird als *weltweite Transformation* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="efd40-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="efd40-108">Die Welt Transformation kann eine einfache affine Transformation oder eine komplexe Sequenz von affinen Transformationen sein, aber unabhängig von ihrer Komplexität ist die globale Transformation in einem einzigen **Matrix** Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="efd40-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="efd40-109">Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse bietet mehrere Methoden zum Aufbauen einer zusammengesetzten Welt Transformation: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)und [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="efd40-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="efd40-110">Im folgenden Beispiel wird eine Ellipse zweimal gezeichnet: einmal vor dem Erstellen einer Welt Transformation und einmal nach.</span><span class="sxs-lookup"><span data-stu-id="efd40-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="efd40-111">Die Transformation skaliert zuerst mit dem Faktor 0,5 in der y-Richtung, übersetzt dann 50 Einheiten in die x-Richtung und dreht dann 30 Grad.</span><span class="sxs-lookup"><span data-stu-id="efd40-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="efd40-112">Die folgende Abbildung zeigt die ursprüngliche Ellipse und die transformierte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="efd40-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![Screenshot eines Fensters, das zwei überlappende Ellipsen enthält. eine ist schmaler und rotiert.](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="efd40-114">Im vorherigen Beispiel wird die Ellipse um den Ursprung des Koordinatensystems gedreht, das sich in der oberen – linken Ecke des Client Bereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="efd40-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="efd40-115">Dies führt zu einem anderen Ergebnis als das Drehen der Ellipse über einen eigenen Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="efd40-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="efd40-116">Eine lokale Transformation ist eine Transformation, die auf ein bestimmtes Element angewendet wird, das gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efd40-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="efd40-117">Ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt verfügt beispielsweise über eine [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) -Methode, die es Ihnen ermöglicht, die Datenpunkte dieses Pfades zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="efd40-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="efd40-118">Im folgenden Beispiel wird ein Rechteck ohne Transformation und ein Pfad mit einer Rotations Transformation gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="efd40-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="efd40-119">(Angenommen, es gibt keine Welt Transformation.)</span><span class="sxs-lookup"><span data-stu-id="efd40-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="efd40-120">Sie können die Welt Transformation mit lokalen Transformationen kombinieren, um eine Vielzahl von Ergebnissen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="efd40-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="efd40-121">Beispielsweise können Sie mit der Welt Transformation das Koordinatensystem überarbeiten und lokale Transformationen verwenden, um Objekte zu drehen und zu skalieren, die auf dem neuen Koordinatensystem gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="efd40-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="efd40-122">Angenommen, Sie möchten ein Koordinatensystem, dessen Ursprung 200 Pixel vom linken Rand des Client Bereichs und 150 Pixel vom oberen Rand des Client Bereichs hat.</span><span class="sxs-lookup"><span data-stu-id="efd40-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="efd40-123">Angenommen, Sie möchten, dass die Maßeinheit das Pixel ist, wobei die x-Achse nach rechts und die y-Achse nach oben zeigt.</span><span class="sxs-lookup"><span data-stu-id="efd40-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="efd40-124">Beim Standard Koordinatensystem wird die y-Achse nach unten angezeigt, sodass Sie eine Reflektion auf der horizontalen Achse ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="efd40-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="efd40-125">Die folgende Abbildung zeigt die Matrix einer solchen Reflektion.</span><span class="sxs-lookup"><span data-stu-id="efd40-125">The following illustration shows the matrix of such a reflection.</span></span>

![Abbildung: eine drei-nach-3-Matrix](images/aboutgdip05-art15.png)

<span data-ttu-id="efd40-127">Nehmen wir als nächstes an, dass Sie eine Translation 200-Einheiten nach rechts und 150-Einheiten ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="efd40-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="efd40-128">Im folgenden Beispiel wird das Koordinatensystem festgelegt, das gerade durch Festlegen der Welt Transformation eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="efd40-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="efd40-129">Der folgende Code (nach dem Code im vorangehenden Beispiel eingefügt) erstellt einen Pfad, der aus einem einzelnen Rechteck mit der unteren linken Ecke am Ursprung des neuen Koordinatensystems besteht.</span><span class="sxs-lookup"><span data-stu-id="efd40-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="efd40-130">Das Rechteck wird einmal ohne lokale Transformation und einmal mit einer lokalen Transformation aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="efd40-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="efd40-131">Die lokale Transformation besteht aus einer horizontalen Skalierung mit dem Faktor 2, gefolgt von einer 30-Grad-Drehung.</span><span class="sxs-lookup"><span data-stu-id="efd40-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="efd40-132">Die folgende Abbildung zeigt das neue Koordinatensystem und die beiden Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="efd40-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![Screenshot einer x-und y-Achse, und ein blaues Quadrat, das von einem semitransparenten rectagle überlagert wurde um die linke untere Ecke gedreht](images/aboutgdip05-art16.png)

 

 



