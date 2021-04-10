---
description: Pixel Nebel erhält seinen Namen aus der Tatsache, dass Sie im Gerätetreiber pro Pixel berechnet wird.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Pixel Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859975"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="90daf-103">Pixel Nebel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="90daf-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="90daf-104">Pixel Nebel erhält seinen Namen aus der Tatsache, dass Sie im Gerätetreiber pro Pixel berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="90daf-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="90daf-105">Dies unterscheidet sich von dem Scheitelpunkt Nebel, der durch die Pipeline während der Transformation und der Beleuchtungsberechnungen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="90daf-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="90daf-106">Pixel Nebel wird manchmal als Tabellen Nebel bezeichnet, da einige Treiber eine vorab berechnete Nachschlage Tabelle verwenden, um den Nebel Faktor zu ermitteln. dabei wird die Tiefe jedes Pixels verwendet, das in Mischungs Berechnungen angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90daf-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="90daf-107">Sie kann mithilfe jeder von Membern des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps identifizierten Nebel Formel angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="90daf-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="90daf-108">Die Implementierungen dieser Formeln sind Treiber spezifisch.</span><span class="sxs-lookup"><span data-stu-id="90daf-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="90daf-109">Wenn ein Treiber eine komplexe Nebel Formel nicht unterstützt, sollte er in eine weniger komplexe Formel herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="90daf-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="90daf-110">Eye-Relative im Vergleich zu Z-basierter Tiefe</span><span class="sxs-lookup"><span data-stu-id="90daf-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="90daf-111">Um Nebel bezogene Grafik Artefakte zu verringern, die durch eine ungleichmäßige Verteilung von z-Werten in einem tiefen Puffer verursacht wurden, verwenden die meisten Hardware Geräte die Augen relative Tiefe anstelle von z-basierten tiefen Werten für Pixel Nebel.</span><span class="sxs-lookup"><span data-stu-id="90daf-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="90daf-112">Die Augen relative Tiefe ist im Grunde das w-Element aus einem homogenen Koordinaten Satz.</span><span class="sxs-lookup"><span data-stu-id="90daf-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="90daf-113">Microsoft Direct3D nimmt die gegenseitige Verwendung des Rhw-Elements aus einem Geräteraum-Koordinaten Satz an, um true w zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="90daf-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="90daf-114">Wenn ein Gerät Eye-relative Nebel unterstützt, wird das **D3DPRASTERCAPS \_ wfog** -Flag im RasterCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur festgelegt, wenn Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="90daf-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="90daf-115">Mit Ausnahme des verweisrasterizers verwenden Software Geräte immer z, um Pixel Nebeleffekte zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="90daf-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="90daf-116">Wenn Eye-relativer Nebel unterstützt wird, verwendet das System automatisch die Augen relative Tiefe anstelle der z-basierten Tiefe, wenn die angegebene Projektions Matrix z-Werte im Raum der Welt erzeugt, die w-Values im Geräteraum entsprechen.</span><span class="sxs-lookup"><span data-stu-id="90daf-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="90daf-117">Sie legen die Projektions Matrix fest, indem Sie die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode aufrufen, indem Sie den D3DTS \_ -Projektions Wert verwenden und eine [**D3DMATRIX**](d3dmatrix.md) -Struktur übergeben, die die gewünschte Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="90daf-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="90daf-118">Wenn die Projektions Matrix mit dieser Anforderung nicht kompatibel ist, werden die Nebeleffekte nicht ordnungsgemäß angewendet.</span><span class="sxs-lookup"><span data-stu-id="90daf-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="90daf-119">Ausführliche Informationen zum Erstellen einer kompatiblen Matrix finden Sie unter [Projektions Transformation (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="90daf-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="90daf-120">Direct3D verwendet die aktuell festgelegte Projektions Matrix in den w-basierten tiefen Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="90daf-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="90daf-121">Daher muss eine Anwendung eine konforme Projektions Matrix festlegen, um die gewünschten w-basierten Funktionen zu erhalten, auch wenn Sie die Direct3D-Transformations Pipeline nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="90daf-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="90daf-122">Direct3D überprüft die vierte Spalte der Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="90daf-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="90daf-123">Wenn die Koeffizienten \[ 0, 0, 0, 1 sind \] (bei einer affinen Projektion), verwendet das System die z-basierten tiefen Werte für den Nebel.</span><span class="sxs-lookup"><span data-stu-id="90daf-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="90daf-124">In diesem Fall müssen Sie auch die Start-und endabstände für lineare Nebeleffekte im Gerätebereich angeben, die von 0,0 am nächsten Punkt bis zum Benutzer und 1,0 am äußersten Punkt liegen.</span><span class="sxs-lookup"><span data-stu-id="90daf-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="90daf-125">Verwenden von Pixel Nebel</span><span class="sxs-lookup"><span data-stu-id="90daf-125">Using Pixel Fog</span></span>

<span data-ttu-id="90daf-126">Verwenden Sie die folgenden Schritte, um Pixel Nebel in Ihrer Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="90daf-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="90daf-127">Aktivieren Sie die Schnebel Mischung, indem Sie den D3DRS \_ fogenable-Rendering-Zustand auf **true** festlegen.</span><span class="sxs-lookup"><span data-stu-id="90daf-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="90daf-128">Legen Sie die gewünschte Nebelfarbe im D3DRS \_ fogcolor-Rendering-Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="90daf-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="90daf-129">Wählen Sie die zu verwendende Nebel Formel aus, indem Sie den \_ renderzustand D3DRS fogtablemode auf den entsprechenden Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festlegen.</span><span class="sxs-lookup"><span data-stu-id="90daf-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="90daf-130">Legen Sie für den ausgewählten Nebelmodus in den zugeordneten renderzuständen die gewünschten Nebel Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="90daf-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="90daf-131">Dies umfasst die Start-und endabstände für linearen Nebel und die Nebeldichte des exponentiellen Nebel Modus.</span><span class="sxs-lookup"><span data-stu-id="90daf-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="90daf-132">Im folgenden Beispiel wird gezeigt, wie diese Schritte im Code aussehen können.</span><span class="sxs-lookup"><span data-stu-id="90daf-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="90daf-133">Einige Nebel Parameter sind als Gleit Komma Werte erforderlich, auch wenn die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode nur DWORD-Werte im zweiten Parameter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="90daf-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="90daf-134">Im vorangehenden Beispiel werden die Gleit Komma Werte für **IDirect3DDevice9:: seetrenderstate** ohne Daten Übersetzung bereitstellt, indem die Adressen der Gleit Komma Variablen als DWORD-Zeiger umgewandelt und dann dereferenzierend durch umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="90daf-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90daf-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90daf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90daf-136">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="90daf-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
