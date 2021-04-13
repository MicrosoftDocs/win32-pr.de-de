---
description: Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine:: setminmaxschnitt-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355147"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="b8cbc-103">ID3DXPRTEngine:: setminmaxschnitt-Methode</span><span class="sxs-lookup"><span data-stu-id="b8cbc-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="b8cbc-104">Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="b8cbc-105">Diese Entfernungs Werte können verwendet werden, um die minimale oder maximale Entfernung zu steuern, die Objekte durch Schatten oder Licht widerspiegeln können.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="b8cbc-106">Beispielsweise kann die-Methode verwendet werden, um den shadodown der in der Nähe befindlichen Funktionen eines 3D-Modells einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cbc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8cbc-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="b8cbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8cbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8cbc-109">der- *Administrator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8cbc-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8cbc-110">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8cbc-111">Minimale Überschneidungs Abweichung.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-111">Minimum intersection distance.</span></span> <span data-ttu-id="b8cbc-112">Muss positiv und kleiner als der Wert von "f" sein.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="b8cbc-113">mit dem Namen  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8cbc-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8cbc-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8cbc-115">Maximale Schnittstellen Länge.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-115">Maximum intersection distance.</span></span> <span data-ttu-id="b8cbc-116">Wenn 0,0 f, wird der vorherige Wert verwendet. Andernfalls muss größer als der Wert von "f" sein.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8cbc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8cbc-117">Return value</span></span>

<span data-ttu-id="b8cbc-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8cbc-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8cbc-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cbc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8cbc-121">Remarks</span></span>

<span data-ttu-id="b8cbc-122">Diese Methode kann nicht in PRT-Simulationen (preberechneten Radiance Transfer) verwendet werden, die in der GPU ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="b8cbc-123">Weitere Informationen finden Sie unter [**ID3DXPRTEngine:: computedirectlightingshgpu**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="b8cbc-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cbc-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8cbc-124">Requirements</span></span>



| <span data-ttu-id="b8cbc-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8cbc-125">Requirement</span></span> | <span data-ttu-id="b8cbc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b8cbc-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cbc-127">Header</span><span class="sxs-lookup"><span data-stu-id="b8cbc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b8cbc-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8cbc-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b8cbc-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8cbc-129">Library</span></span><br/> | <dl> <span data-ttu-id="b8cbc-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8cbc-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8cbc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8cbc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cbc-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b8cbc-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
