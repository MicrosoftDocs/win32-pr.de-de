---
description: Überprüft ein patchmesh und gibt die Anzahl der degenerierten Vertices und Patches zurück.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: D3DXValidPatchMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961583"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="04a3c-103">D3DXValidPatchMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="04a3c-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="04a3c-104">Überprüft ein patchmesh und gibt die Anzahl der degenerierten Vertices und Patches zurück.</span><span class="sxs-lookup"><span data-stu-id="04a3c-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04a3c-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="04a3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04a3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a3c-107">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04a3c-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a3c-108">Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="04a3c-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="04a3c-109">Zeiger auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das zu testende patchmesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="04a3c-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="04a3c-110">*pnumdägeneratevertices* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="04a3c-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04a3c-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04a3c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04a3c-112">Gibt die Anzahl der degenerierten Scheitel Punkte im patchmesh zurück.</span><span class="sxs-lookup"><span data-stu-id="04a3c-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="04a3c-113">*pnumdägeneratepatches* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="04a3c-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04a3c-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04a3c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04a3c-115">Gibt die Anzahl der degenerierten Patches im patchmesh zurück.</span><span class="sxs-lookup"><span data-stu-id="04a3c-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="04a3c-116">*pperrorsandwarning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="04a3c-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04a3c-117">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="04a3c-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="04a3c-118">Gibt einen Zeiger auf einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, in denen die im patchmesh gefundenen Probleme erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="04a3c-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a3c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04a3c-119">Return value</span></span>

<span data-ttu-id="04a3c-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04a3c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04a3c-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04a3c-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04a3c-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="04a3c-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a3c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04a3c-123">Remarks</span></span>

<span data-ttu-id="04a3c-124">Diese Methode überprüft das Mesh, indem auf ungültige Indizes überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="04a3c-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="04a3c-125">Fehlerinformationen sind in der Debugger-Ausgabe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04a3c-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a3c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04a3c-126">Requirements</span></span>



| <span data-ttu-id="04a3c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04a3c-127">Requirement</span></span> | <span data-ttu-id="04a3c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="04a3c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a3c-129">Header</span><span class="sxs-lookup"><span data-stu-id="04a3c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="04a3c-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a3c-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="04a3c-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04a3c-131">Library</span></span><br/> | <dl> <span data-ttu-id="04a3c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04a3c-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04a3c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04a3c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a3c-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="04a3c-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
