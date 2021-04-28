---
description: 'D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h): Berechnet eine Begrenzungskugel für das Gitternetz.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115818"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="67da2-103">D3DXComputeBoundingSphere-Funktion (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="67da2-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="67da2-104">Berechnet eine Begrenzungskugel für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="67da2-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="67da2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67da2-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="67da2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67da2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67da2-107">*pFirstPosition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="67da2-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67da2-108">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="67da2-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67da2-109">Zeiger auf die erste Position.</span><span class="sxs-lookup"><span data-stu-id="67da2-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="67da2-110">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="67da2-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67da2-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67da2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67da2-112">Anzahl der Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="67da2-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="67da2-113">*dwStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="67da2-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67da2-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67da2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67da2-115">Anzahl von Bytes zwischen Positionsvektoren.</span><span class="sxs-lookup"><span data-stu-id="67da2-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="67da2-116">Verwenden [**Sie GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)oder [**D3DXGetDeclVertexSize,**](d3dxgetdeclvertexsize.md) um das Scheitelpunkt-Stride zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="67da2-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="67da2-117">*pCenter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67da2-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67da2-118">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="67da2-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67da2-119">[**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Koordinatenmittelbereich der zurückgegebenen Begrenzungskugel definiert.</span><span class="sxs-lookup"><span data-stu-id="67da2-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="67da2-120">*pRadius* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67da2-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67da2-121">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="67da2-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67da2-122">Radius der zurückgegebenen Begrenzungskugel.</span><span class="sxs-lookup"><span data-stu-id="67da2-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67da2-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67da2-123">Return value</span></span>

<span data-ttu-id="67da2-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67da2-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67da2-125">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67da2-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67da2-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="67da2-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="67da2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67da2-127">Requirements</span></span>



| <span data-ttu-id="67da2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67da2-128">Requirement</span></span> | <span data-ttu-id="67da2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="67da2-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67da2-130">Header</span><span class="sxs-lookup"><span data-stu-id="67da2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="67da2-131"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="67da2-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="67da2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67da2-132">Library</span></span><br/> | <dl> <span data-ttu-id="67da2-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="67da2-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67da2-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67da2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67da2-135">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="67da2-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
