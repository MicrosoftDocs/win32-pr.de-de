---
description: Überprüft ein Mesh.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: D3DXValidMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354607"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="3a376-103">D3DXValidMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a376-103">D3DXValidMesh function</span></span>

<span data-ttu-id="3a376-104">Überprüft ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="3a376-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a376-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a376-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="3a376-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a376-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a376-107">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a376-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a376-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="3a376-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="3a376-109">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zu testende Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a376-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="3a376-110">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a376-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a376-111">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a376-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3a376-112">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im zu testenden Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="3a376-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="3a376-113">*pperrorsandwarning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a376-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a376-114">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a376-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3a376-115">Gibt einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, die die im Mesh gefundenen Probleme erläutern.</span><span class="sxs-lookup"><span data-stu-id="3a376-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a376-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a376-116">Return value</span></span>

<span data-ttu-id="3a376-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a376-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a376-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a376-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a376-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DXERR \_ invalidmesh, D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="3a376-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a376-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a376-120">Remarks</span></span>

<span data-ttu-id="3a376-121">Diese Methode überprüft das Mesh, indem auf ungültige Indizes überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3a376-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="3a376-122">Fehlerinformationen sind in der Debugger-Ausgabe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a376-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a376-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a376-123">Requirements</span></span>



| <span data-ttu-id="3a376-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a376-124">Requirement</span></span> | <span data-ttu-id="3a376-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3a376-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a376-126">Header</span><span class="sxs-lookup"><span data-stu-id="3a376-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3a376-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a376-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3a376-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a376-128">Library</span></span><br/> | <dl> <span data-ttu-id="3a376-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a376-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a376-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a376-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a376-131">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3a376-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
