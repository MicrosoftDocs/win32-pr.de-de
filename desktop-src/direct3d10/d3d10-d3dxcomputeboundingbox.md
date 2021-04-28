---
description: 'D3DXComputeBoundingBox-Funktion (D3DX10math.h): Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.'
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: D3DXComputeBoundingBox-Funktion (D3DX10math.h)
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
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103528"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="0cfd1-103">D3DXComputeBoundingBox-Funktion (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="0cfd1-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="0cfd1-104">Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfd1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cfd1-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="0cfd1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cfd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfd1-107">*pFirstPosition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfd1-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cfd1-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cfd1-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="0cfd1-110">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfd1-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfd1-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cfd1-112">Anzahl der Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0cfd1-113">*dwStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfd1-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfd1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cfd1-115">Anzahl oder Anzahl von Bytes zwischen Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0cfd1-116">*pMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfd1-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfd1-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cfd1-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die zurückgegebene linke untere Ecke des Begrenzungsfelds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="0cfd1-119">*pMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfd1-120">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfd1-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0cfd1-121">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die zurückgegebene rechte obere Ecke des Begrenzungsfelds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfd1-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cfd1-122">Return value</span></span>

<span data-ttu-id="0cfd1-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cfd1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cfd1-124">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0cfd1-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0cfd1-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfd1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cfd1-126">Requirements</span></span>



| <span data-ttu-id="0cfd1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cfd1-127">Requirement</span></span> | <span data-ttu-id="0cfd1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0cfd1-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfd1-129">Header</span><span class="sxs-lookup"><span data-stu-id="0cfd1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0cfd1-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfd1-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="0cfd1-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0cfd1-131">Library</span></span><br/> | <dl> <span data-ttu-id="0cfd1-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cfd1-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cfd1-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0cfd1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfd1-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0cfd1-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
