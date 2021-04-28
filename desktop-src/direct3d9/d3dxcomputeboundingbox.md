---
description: 'D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h): Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.'
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39fdf4123781b84d87ec1c9d790eb5ffae058892
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115828"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="fe9f2-103">D3DXComputeBoundingBox-Funktion (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="fe9f2-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="fe9f2-104">Berechnet ein koordinatenachsenorientiertes Begrenzungsfeld.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe9f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe9f2-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="fe9f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe9f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9f2-107">*pFirstPosition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe9f2-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9f2-108">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe9f2-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9f2-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="fe9f2-110">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe9f2-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9f2-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe9f2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe9f2-112">Anzahl der Scheitelpunkte.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fe9f2-113">*dwStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe9f2-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9f2-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe9f2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe9f2-115">Anzahl oder Anzahl der Bytes zwischen Scheitelpunkten.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fe9f2-116">*pMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe9f2-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9f2-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe9f2-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9f2-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die zurückgegebene linke untere Ecke des umgebenden Felds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="fe9f2-119">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fe9f2-120">*pMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe9f2-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9f2-121">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe9f2-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9f2-122">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die zurückgegebene rechte obere Ecke des umgebenden Felds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="fe9f2-123">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9f2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe9f2-124">Return value</span></span>

<span data-ttu-id="fe9f2-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe9f2-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe9f2-126">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe9f2-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fe9f2-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe9f2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe9f2-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9f2-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe9f2-129">Requirements</span></span>



| <span data-ttu-id="fe9f2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe9f2-130">Requirement</span></span> | <span data-ttu-id="fe9f2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="fe9f2-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9f2-132">Header</span><span class="sxs-lookup"><span data-stu-id="fe9f2-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fe9f2-133"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9f2-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe9f2-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe9f2-134">Library</span></span><br/> | <dl> <span data-ttu-id="fe9f2-135"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe9f2-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe9f2-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe9f2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9f2-137">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe9f2-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
