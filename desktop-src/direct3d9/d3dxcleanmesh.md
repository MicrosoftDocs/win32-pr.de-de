---
description: Bereinigt ein Mesh und bereitet es auf Vereinfachung vor.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: D3DXCleanMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365109"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="7e10f-103">D3DXCleanMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e10f-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="7e10f-104">Bereinigt ein Mesh und bereitet es auf Vereinfachung vor.</span><span class="sxs-lookup"><span data-stu-id="7e10f-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e10f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e10f-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="7e10f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e10f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e10f-107">*Cleantype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-108">Typ: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="7e10f-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="7e10f-109">Vertex-Vorgänge, die zur Vorbereitung der Bereinigung durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e10f-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="7e10f-110">Siehe [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="7e10f-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e10f-111">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-112">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="7e10f-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="7e10f-113">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zu bereinigende Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e10f-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="7e10f-114">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-115">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e10f-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e10f-116">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, die bereinigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e10f-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="7e10f-117">*ppmeshout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-118">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e10f-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7e10f-119">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zurückgegebene bereinigte Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e10f-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="7e10f-120">Das gleiche Mesh wird zurückgegeben, das übergangen wurde, wenn keine Bereinigung notwendig war.</span><span class="sxs-lookup"><span data-stu-id="7e10f-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="7e10f-121">*padjacumcyout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e10f-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e10f-123">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Ausgabe Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="7e10f-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7e10f-124">*pperrorsandwarning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e10f-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10f-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e10f-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7e10f-126">Gibt einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, die die im Mesh gefundenen Probleme erläutern.</span><span class="sxs-lookup"><span data-stu-id="7e10f-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e10f-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e10f-127">Return value</span></span>

<span data-ttu-id="7e10f-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e10f-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e10f-129">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e10f-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e10f-130">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="7e10f-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e10f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e10f-131">Remarks</span></span>

<span data-ttu-id="7e10f-132">Diese Funktion bereinigt ein Mesh mithilfe der Reinigungsmethode und der Optionen, die im cleantype-Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7e10f-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="7e10f-133">Eine Beschreibung der verfügbaren Optionen finden Sie in der [**D3DXCLEANTYPE**](./d3dxcleantype.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="7e10f-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e10f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e10f-134">Requirements</span></span>



| <span data-ttu-id="7e10f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e10f-135">Requirement</span></span> | <span data-ttu-id="7e10f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7e10f-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e10f-137">Header</span><span class="sxs-lookup"><span data-stu-id="7e10f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7e10f-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e10f-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7e10f-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e10f-139">Library</span></span><br/> | <dl> <span data-ttu-id="7e10f-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e10f-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e10f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e10f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e10f-142">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e10f-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
