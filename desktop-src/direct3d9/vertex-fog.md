---
description: Wenn das System vertexfogging ausführt, wendet es bei jedem Scheitelpunkt in einem Polygon eine Nebel Berechnung an und interpoliert die Ergebnisse während der rasterisierung auf der Vorderseite des Polygons.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Scheitelpunkt Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123337"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="f7c2c-103">Scheitelpunkt Nebel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7c2c-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="f7c2c-104">Wenn das System vertexfogging ausführt, wendet es bei jedem Scheitelpunkt in einem Polygon eine Nebel Berechnung an und interpoliert die Ergebnisse während der rasterisierung auf der Vorderseite des Polygons.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="f7c2c-105">Vertex-Nebeleffekte werden von der Direct3D-Beleuchtungs-und-Transformations-Engine berechnet.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="f7c2c-106">Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f7c2c-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="f7c2c-107">Wenn Ihre Anwendung Direct3D nicht für die Transformation und Beleuchtung verwendet, muss die Anwendung Nebel Berechnungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="f7c2c-108">Platzieren Sie in diesem Fall den in der Alpha-Komponente berechneten Nebel Faktor der Glanz Farbe für jeden Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="f7c2c-109">Sie können beliebige Formeln verwenden, die Sie verwenden möchten: Bereichs basiert, Volumetric oder anderweitig.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="f7c2c-110">Direct3D verwendet den angegebenen Nebel Faktor, um das Gesicht jedes Polygons zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="f7c2c-111">Anwendungen, die ihre eigene Transformation und Beleuchtung ausführen, müssen auch eigene Scheitelpunkt Berechnungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="f7c2c-112">Daher muss eine solche Anwendung nur eine Nebel Mischung aktivieren und die Nebelfarbe durch die zugehörigen gerengerzustände festlegen, wie unter [Nebel Mischung (Direct3D 9)](fog-blending.md) und [Nebelfarbe (Direct3D 9)](fog-color.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="f7c2c-113">Wenn Sie einen Vertex-Shader verwenden, müssen Sie Scheitelpunkt Nebel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="f7c2c-114">Dies wird erreicht, indem der Vertex-Shader verwendet wird, um die Nebel Intensität pro Scheitelpunkt in das ofog-Register zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="f7c2c-115">Nachdem der Pixelshader abgeschlossen ist, werden die onebel-Daten für die lineare interinterpolate mit der Nebelfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="f7c2c-116">Diese Intensität ist in einem Pixelshader nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="f7c2c-117">Range-Based Nebel</span><span class="sxs-lookup"><span data-stu-id="f7c2c-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="f7c2c-118">Direct3D verwendet Bereichs basierte Nebel Berechnungen nur bei Verwendung von Scheitelpunkt Nebel mit der Direct3D-Transformation und der Beleuchtungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="f7c2c-119">Der Grund hierfür ist, dass Pixel Nebel im Gerätetreiber implementiert ist und derzeit keine Hardware zur Unterstützung von pro Pixel Bereichs basiertem Nebel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="f7c2c-120">Wenn Ihre Anwendung ihre eigene Transformation und Beleuchtung durchführt, muss Sie eigene, Bereichs basierte oder andere Nebel Berechnungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="f7c2c-121">Manchmal kann die Verwendung von Nebel grafische Artefakte darstellen, die bewirken, dass Objekte in nicht intuitiver Weise mit der Nebelfarbe gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="f7c2c-122">Stellen Sie sich z. b. eine Szene vor, in der zwei sichtbare Objekte vorhanden sind: eine Distanz genug, um von einem Nebel betroffen zu sein, und die andere nahe genug, um nicht betroffen zu sein.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="f7c2c-123">Wenn sich der Anzeigebereich an Ort und Stelle dreht, können sich die offensichtlichen Nebeleffekte ändern, auch wenn die Objekte stationär sind.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="f7c2c-124">Das folgende Diagramm zeigt eine Top-down-Ansicht einer solchen Situation.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-124">The following diagram shows a top-down view of such a situation.</span></span>

![Diagramm mit zwei Standpunkten und deren Auswirkung auf den Nebel für zwei Objekte](images/artifog.png)

<span data-ttu-id="f7c2c-126">Bereichs basierter Nebel ist eine weitere, präzisere Methode zum Ermitteln der Nebeleffekte.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="f7c2c-127">Im Bereichs basierten Nebel verwendet Direct3D die tatsächliche Entfernung von der Sicht Ansicht zu einem Scheitelpunkt für seine Nebel Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="f7c2c-128">Direct3D vergrößert die Auswirkung von Nebel, da der Abstand zwischen den beiden Punkten zunimmt, und nicht die Tiefe des Scheitel Punkts in der Szene. Dadurch werden Rotelle Artefakte vermieden.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="f7c2c-129">Wenn das aktuelle Gerät Bereichs basierten Nebel unterstützt, wird der D3DPRASTERCAPS \_ fogrange-Wert im RasterCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) festgelegt, wenn Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="f7c2c-130">Um Bereichs basierten Nebel zu aktivieren, legen Sie den D3DRS \_ RANGEFOGENABLE-Rendering-Zustand auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="f7c2c-131">Bereichs basierter Nebel wird während der Transformation und Beleuchtung durch Direct3D berechnet.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="f7c2c-132">Anwendungen, die nicht die Direct3D-Transformation und das Beleuchtungs Modul verwenden, müssen auch eigene Scheitelpunkt Berechnungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="f7c2c-133">Geben Sie in diesem Fall den Bereichs basierten Nebel Faktor in der Alpha Komponente der Glanz Komponente für jeden Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="f7c2c-134">Verwenden von Scheitelpunkt Nebel</span><span class="sxs-lookup"><span data-stu-id="f7c2c-134">Using Vertex Fog</span></span>

<span data-ttu-id="f7c2c-135">Führen Sie die folgenden Schritte aus, um den Scheitelpunkt in der Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="f7c2c-136">Aktivieren Sie die Schnebel Mischung \_ , indem Sie D3DRS fogenable auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="f7c2c-137">Legen Sie die Nebelfarbe im D3DRS \_ fogcolor-Rendering-Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="f7c2c-138">Wählen Sie die gewünschte Nebel Formel aus, indem Sie den \_ renderzustand D3DRS fogvertexmode auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="f7c2c-139">Legen Sie die für die ausgewählte Nebel Formel in den Rendering-Zuständen gewünschten Nebel Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="f7c2c-140">Das folgende in C++ geschriebene Beispiel zeigt, wie diese Schritte im Code aussehen können.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="f7c2c-141">Einige Nebel Parameter sind als Gleit Komma Werte erforderlich, auch wenn die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode nur DWORD-Werte im zweiten Parameter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="f7c2c-142">In diesem Beispiel werden die Gleit Komma Werte für diese Methoden ohne Daten Übersetzung erfolgreich bereitstellt, indem die Adressen der Gleit Komma Variablen als DWORD-Zeiger umgewandelt und dann dereferenzierend ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f7c2c-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7c2c-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7c2c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7c2c-144">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="f7c2c-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
