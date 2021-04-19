---
description: Berechnet den Quell Glanz, der sich aus einem einzelnen Sprung der interreflektierten hell mit adaptiver Stichprobenentnahme ergibt.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine:: computebounceadaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353763"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="eae60-103">ID3DXPRTEngine:: computebounceadaptive-Methode</span><span class="sxs-lookup"><span data-stu-id="eae60-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="eae60-104">Berechnet den Quell Glanz, der sich aus einem einzelnen Sprung der interreflektierten hell mit adaptiver Stichprobenentnahme ergibt.</span><span class="sxs-lookup"><span data-stu-id="eae60-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="eae60-105">Diese Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="eae60-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="eae60-106">Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.</span><span class="sxs-lookup"><span data-stu-id="eae60-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae60-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eae60-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="eae60-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eae60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae60-109">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eae60-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-110">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="eae60-111">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt.</span><span class="sxs-lookup"><span data-stu-id="eae60-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="eae60-112">Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="eae60-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="eae60-113">*Adaptivethresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eae60-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eae60-115">Schwellenwert für den PRT-Vektor, der für die Unterteilung von Mesh-Scheitel Punkten und Flächen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="eae60-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="eae60-116">Wenn kleiner als 1E-6f ist, wird ein Standardwert von 1E-6f angegeben.</span><span class="sxs-lookup"><span data-stu-id="eae60-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="eae60-117">*Minedgelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eae60-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eae60-119">Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="eae60-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="eae60-120">Wenn die Methode ermittelt, dass der Wert zu klein ist, wird ein Modell abhängiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="eae60-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="eae60-121">Wenn der Wert NULL ist, wird der Standardwert 4 angegeben.</span><span class="sxs-lookup"><span data-stu-id="eae60-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="eae60-122">*Maxsubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eae60-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eae60-124">Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eae60-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="eae60-125">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eae60-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-126">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="eae60-127">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="eae60-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="eae60-128">Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="eae60-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="eae60-129">*pdatatotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eae60-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eae60-130">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="eae60-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="eae60-131">Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das eine laufende Summe von pdataout für jede Light-Bounce-Berechnung beibehält.</span><span class="sxs-lookup"><span data-stu-id="eae60-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="eae60-132">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="eae60-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eae60-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eae60-133">Return value</span></span>

<span data-ttu-id="eae60-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eae60-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eae60-135">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eae60-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eae60-136">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="eae60-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="eae60-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eae60-137">Requirements</span></span>



| <span data-ttu-id="eae60-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eae60-138">Requirement</span></span> | <span data-ttu-id="eae60-139">Wert</span><span class="sxs-lookup"><span data-stu-id="eae60-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eae60-140">Header</span><span class="sxs-lookup"><span data-stu-id="eae60-140">Header</span></span><br/>  | <dl> <span data-ttu-id="eae60-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae60-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eae60-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eae60-142">Library</span></span><br/> | <dl> <span data-ttu-id="eae60-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eae60-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eae60-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eae60-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae60-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="eae60-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="eae60-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="eae60-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
