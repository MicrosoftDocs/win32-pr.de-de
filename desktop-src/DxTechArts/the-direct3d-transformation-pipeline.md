---
title: Die Direct3D-Transformations Pipeline
description: Dieser Artikel bietet eine technische Erläuterung für Direct3D-Anwendungsentwickler, wie die Parameter der Direct3D-Transformations Pipeline durch direkte Bearbeitung von Direct3D Matrizen festgelegt werden.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869324"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="bf1ed-103">Die Direct3D-Transformations Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf1ed-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="bf1ed-104">Dieser Artikel bietet eine technische Erläuterung für Direct3D-Anwendungsentwickler, wie die Parameter der Direct3D-Transformations Pipeline durch direkte Bearbeitung von Direct3D Matrizen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="bf1ed-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bf1ed-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="bf1ed-106">Transformations Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf1ed-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="bf1ed-107">Verwendungs Tipps</span><span class="sxs-lookup"><span data-stu-id="bf1ed-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="bf1ed-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bf1ed-108">Overview</span></span>

<span data-ttu-id="bf1ed-109">Direct3D verwendet drei Transformationen, um die 3D-Modell Koordinaten in Pixelkoordinaten (Bildschirmraum) zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="bf1ed-110">Diese Transformationen sind Welt Transformation, Ansichts Transformation und Projektions Transformation.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="bf1ed-111">Mit der Welt Transformation wird gesteuert, wie Modell Koordinaten in globale Koordinaten transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="bf1ed-112">Die globale Transformation kann Übersetzungen, Drehungen und Skalierungen enthalten, aber Sie gilt nicht für Leuchten.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="bf1ed-113">Weitere Informationen zum Arbeiten mit weltweiten Transformationen finden Sie unter [Welt Transformation](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="bf1ed-114">View Transform steuert den Übergang von den Weltkoordinaten in den "Kamera Raum", um die Kameraposition weltweit zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="bf1ed-115">Ein Beispiel für das Arbeiten mit Ansichts Transformationen finden Sie unter [View Transform (View Transform](/windows/desktop/direct3d9/view-transform)).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="bf1ed-116">Die Projektions Transformation ändert die Geometrie von Kamerabereich in "Clip Space" und wendet perspektivische Verzerrung an.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="bf1ed-117">Der Begriff "Clip Space" bezieht sich darauf, wie die Geometrie während dieser Transformation auf das Ansichts Volume zugeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="bf1ed-118">Ein Beispiel für das Arbeiten mit Projektions Transformationen finden Sie unter [Projektions Transformation](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="bf1ed-119">Schließlich wird die Geometrie im Clip Bereich in Pixelkoordinaten (Bildschirmraum) transformiert.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="bf1ed-120">Diese Transformation wird durch die viewporteinstellungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="bf1ed-121">Clipping-und transformierende Scheitel Punkte müssen in einem homogenen Raum stattfinden (einfach Leerstellen, in dem das Koordinatensystem ein viertes Element enthält). das Endergebnis für die meisten Anwendungen muss jedoch nicht homogene dreidimensionale (3D-) Koordinaten sein, die im "Bildschirmbereich" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="bf1ed-122">Dies bedeutet, dass sowohl die Eingabe Scheitel Punkte als auch das clippingvolume in homogenen Raum übersetzt werden müssen, um das Clipping auszuführen, und dann wieder in nicht homogenen Bereich übersetzt werden, um angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="bf1ed-123">Die drei Transformationen "Direct3D Transformationen-World", "View" und "Projection" werden durch Direct3D Matrices definiert.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="bf1ed-124">Eine Direct3D-Matrix ist eine homogene 4 x 4-Matrix, die durch eine [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) -Struktur definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="bf1ed-125">Obwohl Direct3D Matrizen keine Standardobjekte sind, werden Sie nicht durch eine COM-Schnittstelle dargestellt. Sie können Sie genauso wie jedes andere Direct3D-Objekt erstellen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="bf1ed-126">Weitere Informationen zu Direct3D Matrizen finden Sie unter [Transformationen](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="bf1ed-127">Transformations Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf1ed-127">The Transformation Pipeline</span></span>

<span data-ttu-id="bf1ed-128">Wenn ein Scheitelpunkt in der Modell Koordinate von pm = (XM, YM, ZM, 1) angegeben wird, werden die in der folgenden Abbildung gezeigten Transformationen auf die Compute-Bildschirm Koordinaten PS = (XS, ys, ZS, WS) angewendet.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![Transformation für Modellraum zu Bildschirmraum](images/d3dxfrm61.gif)

<span data-ttu-id="bf1ed-130">Im folgenden finden Sie Beschreibungen der Stufen, die in der obigen Abbildung dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="bf1ed-131">World Matrix mworld wandelt Scheitel Punkte vom Modellraum in den Raum um.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="bf1ed-132">Diese Matrix wird durch Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="bf1ed-133">Die Direct3D-Implementierung geht davon aus, dass die letzte Spalte dieser Matrix (0,0) ist (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="bf1ed-134">Wenn der Benutzer eine Matrix mit einer anderen letzten Spalte angibt, wird kein Fehler zurückgegeben, aber die Beleuchtung und der Nebel sind falsch.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="bf1ed-135">Anzeigen von Matrix-MVIEW Transformationen Scheitel Punkte aus dem Raum in der Kamera.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="bf1ed-136">Diese Matrix wird durch Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="bf1ed-137">Die Direct3D-Implementierung geht davon aus, dass die letzte Spalte dieser Matrix (0,0) ist (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bf1ed-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="bf1ed-138">Es wird kein Fehler zurückgegeben, wenn der Benutzer eine Matrix mit unterschiedlichen letzten Spalten angibt, aber die Beleuchtung und der Nebel sind falsch.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="bf1ed-139">Projektions Matrix mproj wandelt Scheitel Punkte vom Kamerabereich in den Projektions Bereich um.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="bf1ed-140">Diese Matrix wird durch Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="bf1ed-141">Die letzte Spalte der Projektions Matrix sollte (0, 0, 1, 0) oder (0, 0, a, 0) für korrekte Nebel-und Beleuchtungseffekte lauten. das Formular (0,0) ist bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="bf1ed-142">Das clippingvolume für alle Punkte XP = (XP, YP, ZP, WP) im Projektions Bereich wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="bf1ed-143">Alle Punkte, die diese Gleichungen nicht erfüllen, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="bf1ed-144">Wenn ein Ansichts Volume wie folgt definiert ist:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="bf1ed-145">SW-Bildschirmfenster Breite im Kamerabereich in der Nähe der Clipping-Ebene</span><span class="sxs-lookup"><span data-stu-id="bf1ed-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="bf1ed-146">Höhe des SH-Screen-Fensters im Kamerabereich in der Nähe der Clipping-Ebene</span><span class="sxs-lookup"><span data-stu-id="bf1ed-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="bf1ed-147">HLS-Entfernung zur Near Clipping-Ebene entlang Z-Achsen im Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="bf1ed-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="bf1ed-148">ZF-Entfernung zur weit entfernten Clipping-Ebene entlang Z-Achsen im Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="bf1ed-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="bf1ed-149">Anschließend könnte eine perspektivische Projektions Matrix wie folgt geschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Zeigt eine perspektivische Projektions Matrix an.](images/d3dxfrm62.gif)

    <span data-ttu-id="bf1ed-151">Dabei sind mij Mitglieder von mproj.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="bf1ed-152">Für die orthogonale Projektion haben wir Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-152">For the orthogonal projection we have:</span></span>

    ![orthogonale Projektion](images/d3dxfrm63.gif)

    <span data-ttu-id="bf1ed-154">Direct3D geht davon aus, dass die Perspektiven Projektions Matrix folgendes Format aufweist:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![Perspektiven Projektions Matrix](images/d3dxfrm64.gif)

    <span data-ttu-id="bf1ed-156">Wenn die perspektivische Projektions Matrix nicht über dieses Formular verfügt, werden einige Artefakte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="bf1ed-157">Beispielsweise kann der Tabellen Nebel nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="bf1ed-158">Direct3D ermöglicht dem Benutzer, das Clip Volume wie folgt zu ändern:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![Ändern des clippvolumes](images/d3dxfrm65.gif)

    <span data-ttu-id="bf1ed-160">Dies kann wie folgt umgeschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-160">This can be rewritten as:</span></span>

    ![umgeschriebene Clip Volume ändern](images/d3dxfrm66.gif)

    <span data-ttu-id="bf1ed-162">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="bf1ed-163">Diese Transformation kann eine größere Genauigkeit bieten und entspricht der Skalierung und Verschiebung des clippingvolumes.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="bf1ed-164">Die entsprechende MCLIP-Matrix lautet:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-164">The corresponding Mclip matrix is:</span></span>

    ![MCLIP-Matrix](images/d3dxfrm67.gif)

    <span data-ttu-id="bf1ed-166">Ein Scheitelpunkt wird transformiert durch:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="bf1ed-167">Wenn Sie das Clip Volume nicht skalieren möchten, können Sie Viewport-Parameter auf Standardwerte festlegen:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="bf1ed-168">Die clippingphase ist optional, wenn der Benutzer das D3DDP \_ DoNotClip-Flag in einem drawprimitiven-Befehl angibt.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="bf1ed-169">In diesem Fall können alle Matrizen (einschließlich MVS) kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="bf1ed-170">Die viewportskalierungsmatrix-MVS skaliert die Koordinaten so, dass Sie innerhalb des viewportfensters liegen, und kippt die Y-Achse von oben nach unten:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![Viewport-Skalierungs Matrix-MVS](images/d3dxfrm68.gif)

    <span data-ttu-id="bf1ed-172">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="bf1ed-173">Zum Schluss werden Bildschirm Koordinaten berechnet und an den Rasterizer übermittelt:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![Bildschirm Koordinaten berechnet und an den Raster übermittelt](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="bf1ed-175">Verwendungs Tipps</span><span class="sxs-lookup"><span data-stu-id="bf1ed-175">Usage Tips</span></span>

<span data-ttu-id="bf1ed-176">Im folgenden finden Sie einige Tipps zur Verwendung der Direct3D-Transformations Pipeline:</span><span class="sxs-lookup"><span data-stu-id="bf1ed-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="bf1ed-177">Die letzte Spalte der Welt-und Ansichts Matrizen sollte (0, 0, 0, 1) sein, oder die Beleuchtung ist falsch.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="bf1ed-178">Legen Sie die Viewport-Parameter fest, um eine MCLIP-Identitätsmatrix zu erstellen, es sei denn, Sie wissen genau, wofür Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="bf1ed-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 