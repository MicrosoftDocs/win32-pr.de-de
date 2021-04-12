---
description: Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: D3DXComputeBoundingBox-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219555"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="f7a15-103">D3DXComputeBoundingBox-Funktion (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="f7a15-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="f7a15-104">Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.</span><span class="sxs-lookup"><span data-stu-id="f7a15-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7a15-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="f7a15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7a15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a15-107">*Pfirsich Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a15-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a15-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a15-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f7a15-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="f7a15-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="f7a15-110">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a15-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a15-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7a15-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7a15-112">Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="f7a15-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="f7a15-113">*dwstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a15-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a15-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7a15-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7a15-115">Anzahl oder Anzahl von Bytes zwischen Scheitel Punkten.</span><span class="sxs-lookup"><span data-stu-id="f7a15-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="f7a15-116">*Pmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f7a15-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a15-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a15-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f7a15-118">Ein Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die zurückgegebene untere linke Ecke des umgebenden Felds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f7a15-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="f7a15-119">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f7a15-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7a15-120">*pmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f7a15-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a15-121">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a15-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f7a15-122">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die zurückgegebene obere rechte Ecke des Begrenzungs Rahmens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f7a15-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="f7a15-123">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f7a15-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a15-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7a15-124">Return value</span></span>

<span data-ttu-id="f7a15-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7a15-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7a15-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7a15-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f7a15-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="f7a15-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a15-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7a15-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a15-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7a15-129">Requirements</span></span>



| <span data-ttu-id="f7a15-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7a15-130">Requirement</span></span> | <span data-ttu-id="f7a15-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f7a15-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a15-132">Header</span><span class="sxs-lookup"><span data-stu-id="f7a15-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f7a15-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a15-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f7a15-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7a15-134">Library</span></span><br/> | <dl> <span data-ttu-id="f7a15-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7a15-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7a15-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7a15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a15-137">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f7a15-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
