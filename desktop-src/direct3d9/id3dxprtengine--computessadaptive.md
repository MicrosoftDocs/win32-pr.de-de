---
description: 'Berechnet einen Übertragungs Vektor, der die Quell Strahlung zum Beenden von Strahlen zuordnet, die sich aus der unter Surface-Aufteilung ergeben, wobei Adaptive Stichprobenentnahme und Materialeigenschaften verwendet werden, die von ID3DXPRTEngine:: setmeschmaterials'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine:: computess Adaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365868"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="7cd74-103">ID3DXPRTEngine:: computess Adaptive-Methode</span><span class="sxs-lookup"><span data-stu-id="7cd74-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="7cd74-104">Berechnet einen Übertragungs Vektor, der die Quell Strahlung zum Beenden von Strahlen zuordnet, die sich aus der unter Surface-Aufteilung ergeben, wobei Adaptive Stichprobenentnahme und Materialeigenschaften verwendet werden, die von [**ID3DXPRTEngine:: setmeschmaterials**](id3dxprtengine--setmeshmaterials.md)</span><span class="sxs-lookup"><span data-stu-id="7cd74-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="7cd74-105">Die-Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7cd74-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="7cd74-106">Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7cd74-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cd74-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="7cd74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cd74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd74-109">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-110">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7cd74-111">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7cd74-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="7cd74-112">Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="7cd74-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="7cd74-113">*Adaptivethresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cd74-115">Schwellenwert für den PRT-Vektor, der für die Unterteilung von Mesh-Scheitel Punkten und Flächen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7cd74-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="7cd74-116">Wenn kleiner als 1E-6f ist, wird ein Standardwert von 1E-6f angegeben.</span><span class="sxs-lookup"><span data-stu-id="7cd74-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="7cd74-117">*Minedgelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cd74-119">Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7cd74-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="7cd74-120">Wenn die Methode ermittelt, dass der Wert zu klein ist, wird ein Modell abhängiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="7cd74-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="7cd74-121">*Maxsubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cd74-123">Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cd74-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="7cd74-124">Wenn der Wert NULL ist, wird der Standardwert 4 angegeben.</span><span class="sxs-lookup"><span data-stu-id="7cd74-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="7cd74-125">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-126">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7cd74-127">Ein Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das einen einzelnen Sprung der unter Oberfläche durch verstreut-Licht modelliert.</span><span class="sxs-lookup"><span data-stu-id="7cd74-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="7cd74-128">Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="7cd74-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="7cd74-129">*pdatatotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cd74-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd74-130">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7cd74-131">Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, bei dem es sich um die laufende Summe aller vorherigen pdataout-Ausgaben handelt.</span><span class="sxs-lookup"><span data-stu-id="7cd74-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="7cd74-132">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7cd74-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd74-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cd74-133">Return value</span></span>

<span data-ttu-id="7cd74-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7cd74-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7cd74-135">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7cd74-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7cd74-136">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="7cd74-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd74-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cd74-137">Remarks</span></span>

<span data-ttu-id="7cd74-138">Um die unter Surface-Zerstreuung zu modellieren, wird diese Methode für jeden Licht Sprung aufgerufen, nachdem eine [**ID3DXPRTEngine:: computedirectlightingshadaptive**](id3dxprtengine--computedirectlightingshadaptive.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cd74-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="7cd74-139">Die Ausgabe dieser Methode enthält nicht "Albedo", und nur das eingehende Licht ist in den Simulator integriert.</span><span class="sxs-lookup"><span data-stu-id="7cd74-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="7cd74-140">Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.</span><span class="sxs-lookup"><span data-stu-id="7cd74-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="7cd74-141">[**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) aufzurufen, um jeden PRT-Vektor von Albedo zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="7cd74-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd74-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cd74-142">Requirements</span></span>



| <span data-ttu-id="7cd74-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cd74-143">Requirement</span></span> | <span data-ttu-id="7cd74-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7cd74-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd74-145">Header</span><span class="sxs-lookup"><span data-stu-id="7cd74-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7cd74-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd74-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7cd74-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7cd74-147">Library</span></span><br/> | <dl> <span data-ttu-id="7cd74-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cd74-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7cd74-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cd74-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd74-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="7cd74-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="7cd74-151">**ID3DXPRTEngine:: computebounce**</span><span class="sxs-lookup"><span data-stu-id="7cd74-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="7cd74-152">**ID3DXPRTEngine:: computess**</span><span class="sxs-lookup"><span data-stu-id="7cd74-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
