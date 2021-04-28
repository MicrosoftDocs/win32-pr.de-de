---
description: 'D3DXComputeBoundingSphere-Funktion (D3DX10math.h): Berechnet eine umgebende Kugel für das Netz.'
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: D3DXComputeBoundingSphere-Funktion (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113298"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="38bea-103">D3DXComputeBoundingSphere-Funktion (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="38bea-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="38bea-104">Berechnet eine umschließende Kugel für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="38bea-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="38bea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38bea-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="38bea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38bea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38bea-107">*pFirstPosition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bea-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bea-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38bea-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="38bea-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="38bea-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="38bea-110">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bea-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bea-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38bea-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38bea-112">Anzahl der Scheitelpunkte.</span><span class="sxs-lookup"><span data-stu-id="38bea-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="38bea-113">*dwStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bea-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bea-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38bea-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38bea-115">Anzahl der Bytes zwischen Positionsvektoren.</span><span class="sxs-lookup"><span data-stu-id="38bea-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="38bea-116">*pCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bea-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bea-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="38bea-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="38bea-118">[**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die den Koordinatenmittelpunkt der zurückgegebenen umgebenden Kugel definiert.</span><span class="sxs-lookup"><span data-stu-id="38bea-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="38bea-119">*pRadius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="38bea-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38bea-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38bea-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38bea-121">Radius der zurückgegebenen umgebenden Kugel.</span><span class="sxs-lookup"><span data-stu-id="38bea-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38bea-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38bea-122">Return value</span></span>

<span data-ttu-id="38bea-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38bea-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38bea-124">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38bea-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38bea-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="38bea-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="38bea-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38bea-126">Requirements</span></span>



| <span data-ttu-id="38bea-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38bea-127">Requirement</span></span> | <span data-ttu-id="38bea-128">Wert</span><span class="sxs-lookup"><span data-stu-id="38bea-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38bea-129">Header</span><span class="sxs-lookup"><span data-stu-id="38bea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="38bea-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="38bea-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="38bea-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38bea-131">Library</span></span><br/> | <dl> <span data-ttu-id="38bea-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38bea-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38bea-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38bea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38bea-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="38bea-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
