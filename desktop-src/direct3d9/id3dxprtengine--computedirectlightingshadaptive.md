---
description: Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung mithilfe der adaptiven Stichprobenentnahme durch eine Glanz Näherung (SH) dargestellt wird.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine:: computedirectlightingshadaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762375"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="8517e-103">ID3DXPRTEngine:: computedirectlightingshadaptive-Methode</span><span class="sxs-lookup"><span data-stu-id="8517e-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="8517e-104">Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung mithilfe der adaptiven Stichprobenentnahme durch eine Glanz Näherung (SH) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8517e-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="8517e-105">Diese Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8517e-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="8517e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8517e-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="8517e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8517e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8517e-108">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8517e-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8517e-109">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8517e-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8517e-110">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="8517e-110">Order of the SH evaluation.</span></span> <span data-ttu-id="8517e-111">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="8517e-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="8517e-112">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="8517e-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8517e-113">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="8517e-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="8517e-114">*Adaptivethresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8517e-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8517e-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8517e-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8517e-116">Schwellenwert für den PRT-Vektor, der für die Unterteilung von Mesh-Scheitel Punkten und Flächen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8517e-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="8517e-117">Wenn kleiner als 1E-6f ist, wird ein Standardwert von 1E-6f angegeben.</span><span class="sxs-lookup"><span data-stu-id="8517e-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8517e-118">*Minedgelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8517e-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8517e-119">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8517e-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8517e-120">Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8517e-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="8517e-121">Wenn die Methode ermittelt, dass der Wert zu klein ist, wird ein Modell abhängiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="8517e-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="8517e-122">Wenn der Wert NULL ist, wird der Standardwert 4 angegeben.</span><span class="sxs-lookup"><span data-stu-id="8517e-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8517e-123">*Maxsubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8517e-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8517e-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8517e-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8517e-125">Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8517e-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="8517e-126">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8517e-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8517e-127">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8517e-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8517e-128">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8517e-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="8517e-129">Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="8517e-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8517e-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8517e-130">Return value</span></span>

<span data-ttu-id="8517e-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8517e-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8517e-132">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8517e-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8517e-133">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="8517e-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8517e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8517e-134">Requirements</span></span>



| <span data-ttu-id="8517e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8517e-135">Requirement</span></span> | <span data-ttu-id="8517e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8517e-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8517e-137">Header</span><span class="sxs-lookup"><span data-stu-id="8517e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="8517e-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8517e-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8517e-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8517e-139">Library</span></span><br/> | <dl> <span data-ttu-id="8517e-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8517e-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8517e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8517e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8517e-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="8517e-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="8517e-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="8517e-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
