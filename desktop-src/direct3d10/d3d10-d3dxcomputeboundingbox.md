---
description: Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: D3DXComputeBoundingBox-Funktion (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370451"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="71646-103">D3DXComputeBoundingBox-Funktion (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="71646-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="71646-104">Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.</span><span class="sxs-lookup"><span data-stu-id="71646-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="71646-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71646-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="71646-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71646-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71646-107">*Pfirsich Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71646-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71646-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="71646-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="71646-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="71646-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="71646-110">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71646-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71646-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71646-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71646-112">Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="71646-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="71646-113">*dwstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71646-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71646-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71646-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71646-115">Anzahl oder Anzahl von Bytes zwischen Scheitel Punkten.</span><span class="sxs-lookup"><span data-stu-id="71646-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="71646-116">*Pmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71646-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71646-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="71646-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="71646-118">Ein Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die zurückgegebene untere linke Ecke des umgebenden Felds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="71646-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="71646-119">*pmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71646-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71646-120">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="71646-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="71646-121">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die zurückgegebene obere rechte Ecke des Begrenzungs Rahmens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="71646-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71646-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71646-122">Return value</span></span>

<span data-ttu-id="71646-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71646-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71646-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71646-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="71646-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="71646-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="71646-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71646-126">Requirements</span></span>



| <span data-ttu-id="71646-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71646-127">Requirement</span></span> | <span data-ttu-id="71646-128">Wert</span><span class="sxs-lookup"><span data-stu-id="71646-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71646-129">Header</span><span class="sxs-lookup"><span data-stu-id="71646-129">Header</span></span><br/>  | <dl> <span data-ttu-id="71646-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="71646-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="71646-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71646-131">Library</span></span><br/> | <dl> <span data-ttu-id="71646-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71646-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71646-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71646-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71646-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="71646-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
