---
description: Berechnet eine umgebende Kugel für das Mesh.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: D3DXComputeBoundingSphere-Funktion (D3DX10math. h)
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
ms.openlocfilehash: 0c8e59b4d39652d02ce19f4c1bf6b0617fee7772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219638"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="6f116-103">D3DXComputeBoundingSphere-Funktion (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="6f116-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="6f116-104">Berechnet eine umgebende Kugel für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="6f116-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f116-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f116-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="6f116-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f116-107">*Pfirsich Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f116-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f116-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f116-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f116-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="6f116-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="6f116-110">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f116-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f116-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f116-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f116-112">Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="6f116-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="6f116-113">*dwstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f116-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f116-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f116-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f116-115">Anzahl von Bytes zwischen Positions Vektoren.</span><span class="sxs-lookup"><span data-stu-id="6f116-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="6f116-116">*pcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f116-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f116-117">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f116-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f116-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die das Koordinaten Zentrum der zurückgegebenen Begrenzungs Kugel definiert.</span><span class="sxs-lookup"><span data-stu-id="6f116-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="6f116-119">*pradius* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f116-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f116-120">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f116-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f116-121">Der Radius der zurückgegebenen Begrenzungs Kugel.</span><span class="sxs-lookup"><span data-stu-id="6f116-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f116-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f116-122">Return value</span></span>

<span data-ttu-id="6f116-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f116-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f116-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f116-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6f116-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="6f116-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f116-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f116-126">Requirements</span></span>



| <span data-ttu-id="6f116-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f116-127">Requirement</span></span> | <span data-ttu-id="6f116-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6f116-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f116-129">Header</span><span class="sxs-lookup"><span data-stu-id="6f116-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6f116-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f116-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="6f116-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f116-131">Library</span></span><br/> | <dl> <span data-ttu-id="6f116-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f116-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f116-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f116-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f116-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6f116-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
