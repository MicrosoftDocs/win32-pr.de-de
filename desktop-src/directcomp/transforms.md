---
title: Transformationen (DirectComposition)
description: In diesem Thema wird die Microsoft DirectComposition-Unterstützung für zweidimensionale (2D) affine (lineare) Transformationen und die Typen von Transformationen beschrieben, die DirectComposition unterstützt.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118655"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="71a62-103">Transformationen (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="71a62-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="71a62-104">Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="71a62-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="71a62-105">Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene.](/windows/uwp/composition/visual-layer-in-desktop-apps)</span><span class="sxs-lookup"><span data-stu-id="71a62-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="71a62-106">In diesem Thema wird die Microsoft DirectComposition-Unterstützung für zweidimensionale (2D) affine (lineare) Transformationen und die Typen von Transformationen beschrieben, die DirectComposition unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71a62-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="71a62-107">DirectComposition unterstützt auch 3D-Perspektiventransformationen, aber da sie die Erstellung einer Zwischenbitmap erfordern, betrachtet DirectComposition sie als Effekte und nicht als Transformationen.</span><span class="sxs-lookup"><span data-stu-id="71a62-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="71a62-108">Informationen zu 3D-Perspektivtransformationseffekten finden Sie unter [Effekte](effects.md).</span><span class="sxs-lookup"><span data-stu-id="71a62-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="71a62-109">Dieses Thema enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="71a62-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="71a62-110">Was ist eine DirectComposition 2D-Transformation?</span><span class="sxs-lookup"><span data-stu-id="71a62-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="71a62-111">Der DirectComposition 2D-Koordinatenraum</span><span class="sxs-lookup"><span data-stu-id="71a62-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="71a62-112">Unterstützung für affine 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="71a62-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="71a62-113">Matrix-2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="71a62-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="71a62-114">Transformieren von Gruppen</span><span class="sxs-lookup"><span data-stu-id="71a62-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="71a62-115">Transformationsanimation</span><span class="sxs-lookup"><span data-stu-id="71a62-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="71a62-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="71a62-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="71a62-117">Was ist eine DirectComposition 2D-Transformation?</span><span class="sxs-lookup"><span data-stu-id="71a62-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="71a62-118">Mit einer 2D-Transformation können Sie die Position, Größe oder Art eines Visuals in zwei Dimensionen ändern, indem Sie das Visual an eine andere Position verschieben (Übersetzung), es vergrößern oder verkleinern (skalieren), es drehen (Drehung) oder seine Form verzerren (Verzerrung).</span><span class="sxs-lookup"><span data-stu-id="71a62-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="71a62-119">Eine 2D-Transformation wird erreicht, indem die Punkte eines Visuals von einer Position zu einer anderen innerhalb desselben Koordinatenraums oder von einem Koordinatenraum zu einem anderen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="71a62-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="71a62-120">Diese Zuordnung wird durch eine Tabelle mit Werten beschrieben, die als Transformationsmatrix bezeichnet wird und als Auflistung von drei Zeilen mit drei Spalten mit Gleitkommawerten definiert ist, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="71a62-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="71a62-121">M11Standard: 1.0</span><span class="sxs-lookup"><span data-stu-id="71a62-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="71a62-122">M21Standard: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="71a62-123">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="71a62-124">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="71a62-125">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="71a62-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="71a62-126">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="71a62-127">0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-127">0.0</span></span><br/>
        <span data-ttu-id="71a62-128">0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-128">0.0</span></span><br/>
        <span data-ttu-id="71a62-129">1,0</span><span class="sxs-lookup"><span data-stu-id="71a62-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="71a62-130">Die Transformationsmatrix für affine 2D-Transformationen ist eine 3:2-Matrix, die die dritte Spalte aus der vorherigen Transformationsmatrix ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="71a62-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="71a62-131">Die folgende Tabelle zeigt das Layout dieser Matrix.</span><span class="sxs-lookup"><span data-stu-id="71a62-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="71a62-132">M11Standard: 1.0</span><span class="sxs-lookup"><span data-stu-id="71a62-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="71a62-133">M21Standard: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="71a62-134">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="71a62-135">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="71a62-136">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="71a62-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="71a62-137">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="71a62-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="71a62-138">DirectComposition führt beim Anwenden von 2D-Transformationen auf Stereoinhalte keine spezielle Verarbeitung durch.</span><span class="sxs-lookup"><span data-stu-id="71a62-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="71a62-139">Dies bedeutet, dass der 3D-Inhalt möglicherweise verzerrt erscheint, wenn eine 2D-Transformation darauf angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="71a62-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="71a62-140">Der DirectComposition 2D-Koordinatenraum</span><span class="sxs-lookup"><span data-stu-id="71a62-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="71a62-141">DirectComposition verwendet einen linkshändigen 2D-Koordinatenraum. Das bedeutet, dass positive Werte der X-Achse nach rechts und positive Werte der y-Achse nach unten zunehmen.</span><span class="sxs-lookup"><span data-stu-id="71a62-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="71a62-142">Visuals werden relativ zum Ursprung positioniert. Dies ist der Punkt, an dem sich die x-Achse und die y-Achse überschneiden (0, 0), wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="71a62-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![x-Achse und y-Achse eines linkshändigen Koordinatenraums](images/coordinatespace.png)

<span data-ttu-id="71a62-144">Indem Sie Werte in einer 3 by 2-Transformationsmatrix bearbeiten, können Sie ein Objekt in zwei Dimensionen drehen, skalieren, verschiegen und übersetzen.</span><span class="sxs-lookup"><span data-stu-id="71a62-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="71a62-145">Wenn Sie beispielsweise OffsetX auf 100 und OffsetY auf 200 festlegen, verschieben Sie das Objekt um 100 Pixel nach rechts und 200 Pixel nach unten.</span><span class="sxs-lookup"><span data-stu-id="71a62-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="71a62-146">Unterstützung für affine 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="71a62-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="71a62-147">Die folgende Tabelle beschreibt die Typen von affinen 2D-Transformationen, die von DirectComposition unterstützt werden, und listet die Schnittstellen auf, die Sie zum Ausführen der verschiedenen Arten von Transformationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="71a62-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="71a62-148">Transformieren/Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71a62-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="71a62-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71a62-149">Description</span></span>                                                                                              | <span data-ttu-id="71a62-150">Abbildung</span><span class="sxs-lookup"><span data-stu-id="71a62-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a62-151">Rotieren der [**2D-Idcompositionrotatetransform-Neulinie**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[\]</span><span class="sxs-lookup"><span data-stu-id="71a62-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="71a62-152">Drehen Sie ein Visual um den angegebenen Winkel um den angegebenen Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="71a62-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![Abbildung eines Quadrats, das um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht wurde](images/rotate.png)               |
| <span data-ttu-id="71a62-154">Skalieren einer [**2D-IDcompositionscaletransform-Neulinie**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[\]</span><span class="sxs-lookup"><span data-stu-id="71a62-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="71a62-155">skalieren Sie ein Visual um den angegebenen Faktor um den angegebenen Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="71a62-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![Abbildung eines quadratisch skalierten 130 Prozent](images/scale.png)                                                                  |
| <span data-ttu-id="71a62-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="71a62-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="71a62-158">Verzerrt ein Visuelles um den angegebenen Winkel entlang der X- und y-Achse und um den angegebenen Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="71a62-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![Abbildung einer quadratischen Schiefe von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew.png)                                   |
| <span data-ttu-id="71a62-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="71a62-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="71a62-161">Ändert die Position eines Visuals in Richtung der x-Achse und der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="71a62-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![Abbildung eines Quadrats, das 20 Einheiten entlang der positiven X-Achse und 10 Einheiten entlang der positiven Y-Achse verschoben wurde](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="71a62-163">Matrix-2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="71a62-163">Matrix 2D transforms</span></span>

<span data-ttu-id="71a62-164">Mit [**der IDCompositionMatrixTransform-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) können Sie Eine eigene 3-by-2-affine 2D-Transformationsmatrix definieren und auf ein Visual anwenden.</span><span class="sxs-lookup"><span data-stu-id="71a62-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="71a62-165">Diese Schnittstelle ist nützlich, wenn Sie einen Typ der affinen 2D-Transformation anwenden müssen, der nicht über die anderen DirectComposition-Transformationsschnittstellen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="71a62-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="71a62-166">Sie definieren die Matrix, indem Sie eine [**D2D \_ MATRIX \_ 3X2 \_ F-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) ausfüllen und an die [**IDCompositionMatrixTransform::SetMatrix-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) übergeben.</span><span class="sxs-lookup"><span data-stu-id="71a62-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="71a62-167">Transformieren von Gruppen</span><span class="sxs-lookup"><span data-stu-id="71a62-167">Transform Groups</span></span>

<span data-ttu-id="71a62-168">Sie können Transformationsgruppen verwenden, um mehrere Transformationen zu einer Transformation zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="71a62-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="71a62-169">Eine Transformationsgruppe definiert eine Auflistung von Transformationsobjekten, deren Matrizen in der Reihenfolge, in der sie in der Auflistung angegeben sind, multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="71a62-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="71a62-170">Die resultierende Transformationsmatrix wird dann auf das Visual angewendet.</span><span class="sxs-lookup"><span data-stu-id="71a62-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="71a62-171">Eine Transformationsgruppe erzeugt das gleiche Ergebnis wie das separat anwenden jeder Transformation.</span><span class="sxs-lookup"><span data-stu-id="71a62-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="71a62-172">Beachten Sie, dass die Reihenfolge der Transformationsobjekte in einer Transformationsgruppe wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="71a62-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="71a62-173">Wenn z. B. ein Visual zuerst gedreht, dann skaliert und dann übersetzt wird, ist das Ergebnis anders als wenn das Visual zuerst übersetzt, dann gedreht und dann skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="71a62-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="71a62-174">DirectComposition wendet die Transformationen immer in der Reihenfolge auf ein Visual an, in der sie in der Auflistung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="71a62-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="71a62-175">Um eine Transformationsgruppe zu erstellen, erstellen Sie zuerst die Transformationsobjekte, die Sie in die Gruppe enthalten möchten, und übergeben dann ein Array von Transformationsobjektzetern an die [**IDCompositionDevice::CreateTransformGroup-Methode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup)</span><span class="sxs-lookup"><span data-stu-id="71a62-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="71a62-176">Nachdem Sie eine Transformationsgruppe erstellt haben, können Sie keine Transformationsobjekte hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="71a62-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="71a62-177">Sie können jedoch die Eigenschaften der einzelnen Transformationsobjekte in der Auflistung ändern, und die Änderungen werden in der resultierenden Transformationsmatrix widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="71a62-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="71a62-178">Transformationsanimation</span><span class="sxs-lookup"><span data-stu-id="71a62-178">Transform animation</span></span>

<span data-ttu-id="71a62-179">Die Eigenschaften einer Transformation können animiert werden.</span><span class="sxs-lookup"><span data-stu-id="71a62-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="71a62-180">Wenn eine Eigenschaft animiert wird, ändert DirectComposition den Wert der Eigenschaft im Laufe der Zeit und nicht alle auf einmal.</span><span class="sxs-lookup"><span data-stu-id="71a62-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="71a62-181">Dies ist besonders nützlich, wenn Übergänge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="71a62-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="71a62-182">Weitere Informationen finden Sie unter [Animation](animation.md).</span><span class="sxs-lookup"><span data-stu-id="71a62-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71a62-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71a62-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71a62-184">DirectComposition-Konzepte</span><span class="sxs-lookup"><span data-stu-id="71a62-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
