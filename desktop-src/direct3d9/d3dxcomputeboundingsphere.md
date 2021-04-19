---
description: Berechnet eine umgebende Kugel für das Mesh.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: D3DXComputeBoundingSphere-Funktion (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9e6a0c9fb67abe8a98ccf8b3f9b895fd63fc3e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366653"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="65d9a-103">D3DXComputeBoundingSphere-Funktion (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="65d9a-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="65d9a-104">Berechnet eine umgebende Kugel für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="65d9a-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65d9a-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="65d9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d9a-107">*Pfirsich Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65d9a-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d9a-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="65d9a-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="65d9a-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="65d9a-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="65d9a-110">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65d9a-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d9a-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65d9a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65d9a-112">Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="65d9a-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="65d9a-113">*dwstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65d9a-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d9a-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65d9a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65d9a-115">Anzahl von Bytes zwischen Positions Vektoren.</span><span class="sxs-lookup"><span data-stu-id="65d9a-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="65d9a-116">Verwenden Sie [**getnumbytespertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)oder [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) , um den Scheitelpunkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="65d9a-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="65d9a-117">*pcenter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65d9a-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65d9a-118">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="65d9a-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="65d9a-119">[**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Koordinaten Zentrum der zurückgegebenen Begrenzungs Kugel definiert.</span><span class="sxs-lookup"><span data-stu-id="65d9a-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="65d9a-120">*pradius* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65d9a-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65d9a-121">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="65d9a-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="65d9a-122">Der Radius der zurückgegebenen Begrenzungs Kugel.</span><span class="sxs-lookup"><span data-stu-id="65d9a-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d9a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65d9a-123">Return value</span></span>

<span data-ttu-id="65d9a-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65d9a-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65d9a-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65d9a-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65d9a-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="65d9a-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d9a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65d9a-127">Requirements</span></span>



| <span data-ttu-id="65d9a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65d9a-128">Requirement</span></span> | <span data-ttu-id="65d9a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="65d9a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65d9a-130">Header</span><span class="sxs-lookup"><span data-stu-id="65d9a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="65d9a-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d9a-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="65d9a-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65d9a-132">Library</span></span><br/> | <dl> <span data-ttu-id="65d9a-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65d9a-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65d9a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65d9a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d9a-135">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="65d9a-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
