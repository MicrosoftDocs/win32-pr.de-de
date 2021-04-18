---
description: Generiert eine optimierte Gesichts Zuordnung für eine Dreiecks Liste.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: D3DXOptimizeFaces-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351918"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="a9fb3-103">D3DXOptimizeFaces-Funktion</span><span class="sxs-lookup"><span data-stu-id="a9fb3-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="a9fb3-104">Generiert eine optimierte Gesichts Zuordnung für eine Dreiecks Liste.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fb3-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="a9fb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fb3-107">*PIndizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9fb3-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb3-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9fb3-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9fb3-109">Zeiger auf Dreiecks Listenindizes, die zum Anordnen von Scheitel Punkten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb3-110">*Numerische Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9fb3-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb3-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9fb3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9fb3-112">Anzahl der Gesichter in der Dreiecks Liste.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="a9fb3-113">Bei 16-Bit-Meshes ist dies auf 2 ^ 16-1 (65535) oder weniger Gesichter beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb3-114">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9fb3-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb3-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9fb3-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9fb3-116">Anzahl der Scheitel Punkte, auf die durch die Dreiecks Liste verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="a9fb3-117">*Indices32Bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9fb3-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb3-118">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9fb3-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9fb3-119">Flag, das den Indextyp angibt: **true** , wenn Indizes 32-Bit (mehr als 65535 Indizes) sind, **false** , wenn Indizes 16-Bit (65535 oder weniger Indizes) sind.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="a9fb3-120">*pfakeremap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a9fb3-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fb3-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fb3-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9fb3-122">Zeiger auf das ursprüngliche Gitter Gesicht, das geteilt wurde, um die aktuelle Seite zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fb3-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9fb3-123">Return value</span></span>

<span data-ttu-id="a9fb3-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9fb3-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9fb3-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9fb3-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9fb3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9fb3-127">Remarks</span></span>

<span data-ttu-id="a9fb3-128">Die Optimierungs Prozedur dieser Funktion ist funktional äquivalent zum Aufrufen von [**ID3DXMesh::**](id3dxmesh--optimize.md) Optimization mit dem D3DXMESHOPT \_ deviceindependent-Flag. diese Funktion ermöglicht jedoch eine effizientere Verwendung von Scheitelpunkt Caches.</span><span class="sxs-lookup"><span data-stu-id="a9fb3-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fb3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9fb3-129">Requirements</span></span>



| <span data-ttu-id="a9fb3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9fb3-130">Requirement</span></span> | <span data-ttu-id="a9fb3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a9fb3-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fb3-132">Header</span><span class="sxs-lookup"><span data-stu-id="a9fb3-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a9fb3-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fb3-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a9fb3-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9fb3-134">Library</span></span><br/> | <dl> <span data-ttu-id="a9fb3-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9fb3-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9fb3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9fb3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fb3-137">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a9fb3-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
