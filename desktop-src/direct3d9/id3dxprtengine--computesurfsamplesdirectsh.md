---
description: Berechnet an einem beliebigen Punkt, der nicht in einem Mesh ist, einen Übertragungs Vektor, der Quell Strahlen (dargestellt durch eine Glanz Näherung (SH)) zum Beenden der Strahlung zuordnet.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'ID3DXPRTEngine:: computesurf samplesdirectsh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356046"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="fd529-103">ID3DXPRTEngine:: computesurf samplesdirectsh-Methode</span><span class="sxs-lookup"><span data-stu-id="fd529-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="fd529-104">Berechnet an einem beliebigen Punkt, der nicht in einem Mesh ist, einen Übertragungs Vektor, der Quell Strahlen (dargestellt durch eine Glanz Näherung (SH)) zum Beenden der Strahlung zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fd529-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd529-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd529-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="fd529-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd529-107">*Shorder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd529-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd529-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd529-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd529-109">Die Reihenfolge der zu verwendenden SH-Näherung.</span><span class="sxs-lookup"><span data-stu-id="fd529-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="fd529-110">*NumSamples* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd529-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd529-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd529-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd529-112">Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="fd529-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="fd529-113">*psamplelocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd529-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd529-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd529-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd529-115">Die Position für jede Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="fd529-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="fd529-116">*psamplenorms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd529-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd529-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd529-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd529-118">Normaler Vektor für jeden Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="fd529-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="fd529-119">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd529-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd529-120">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="fd529-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="fd529-121">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das den direkten Beleuchtungs Beitrag zu dem Punkt modelliert und dabei die sh-Näherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd529-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd529-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd529-122">Return value</span></span>

<span data-ttu-id="fd529-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd529-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd529-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fd529-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fd529-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="fd529-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd529-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd529-126">Remarks</span></span>

<span data-ttu-id="fd529-127">Verwenden Sie beim Aufrufen dieser Methode keinen Textur Puffer.</span><span class="sxs-lookup"><span data-stu-id="fd529-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd529-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd529-128">Requirements</span></span>



| <span data-ttu-id="fd529-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd529-129">Requirement</span></span> | <span data-ttu-id="fd529-130">Wert</span><span class="sxs-lookup"><span data-stu-id="fd529-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd529-131">Header</span><span class="sxs-lookup"><span data-stu-id="fd529-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fd529-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd529-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fd529-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd529-133">Library</span></span><br/> | <dl> <span data-ttu-id="fd529-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd529-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd529-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd529-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd529-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fd529-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="fd529-137">**ID3DXPRTEngine:: computedirectlightingsh**</span><span class="sxs-lookup"><span data-stu-id="fd529-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="fd529-138">**ID3DXPRTEngine:: computesurf samplesbounce**</span><span class="sxs-lookup"><span data-stu-id="fd529-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
