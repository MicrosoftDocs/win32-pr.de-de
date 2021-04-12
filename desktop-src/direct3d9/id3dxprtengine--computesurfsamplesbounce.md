---
description: Berechnet PRT-Proben (preberechneten Radiance Transfer) für einen beliebigen Punkt (und den normalen Vektor).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine:: computesurf samplesbounce-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356056"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="2a1bc-103">ID3DXPRTEngine:: computesurf samplesbounce-Methode</span><span class="sxs-lookup"><span data-stu-id="2a1bc-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="2a1bc-104">Berechnet PRT-Proben (preberechneten Radiance Transfer) für einen beliebigen Punkt (und den normalen Vektor).</span><span class="sxs-lookup"><span data-stu-id="2a1bc-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a1bc-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="2a1bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a1bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a1bc-107">*psurfdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-108">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2a1bc-109">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das die Quell Ausstrahlung des 3D-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="2a1bc-110">Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="2a1bc-111">*NumSamples* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a1bc-113">Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="2a1bc-114">*psamplelocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-115">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a1bc-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2a1bc-116">Die Position für jede Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="2a1bc-117">*psamplenorms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-118">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a1bc-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2a1bc-119">Normaler Vektor für jeden Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="2a1bc-120">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-121">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2a1bc-122">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das den direkten Beleuchtungs Beitrag zu dem Punkt modelliert, indem die Näherung für die kugelförmige harmonische (SH) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="2a1bc-123">*pdatatotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a1bc-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a1bc-124">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2a1bc-125">Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, bei dem es sich um die laufende Summe aller vorherigen pdataout-Ausgaben handelt.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="2a1bc-126">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a1bc-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a1bc-127">Return value</span></span>

<span data-ttu-id="2a1bc-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a1bc-129">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a1bc-130">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="2a1bc-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1bc-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a1bc-131">Requirements</span></span>



| <span data-ttu-id="2a1bc-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a1bc-132">Requirement</span></span> | <span data-ttu-id="2a1bc-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2a1bc-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1bc-134">Header</span><span class="sxs-lookup"><span data-stu-id="2a1bc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2a1bc-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1bc-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2a1bc-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a1bc-136">Library</span></span><br/> | <dl> <span data-ttu-id="2a1bc-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a1bc-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a1bc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a1bc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1bc-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="2a1bc-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="2a1bc-140">**ID3DXPRTEngine:: computesurf samplesdirectsh**</span><span class="sxs-lookup"><span data-stu-id="2a1bc-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
