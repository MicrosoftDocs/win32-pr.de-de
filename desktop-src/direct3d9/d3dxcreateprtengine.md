---
description: Erstellt ein ID3DXPRTEngine-Objekt, das die PRT-Simulationen (preberechnete Strahlen Übertragung) einer 3D-Szene effizient generieren kann.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: D3DXCreatePRTEngine-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530929"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="95f1e-103">D3DXCreatePRTEngine-Funktion</span><span class="sxs-lookup"><span data-stu-id="95f1e-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="95f1e-104">Erstellt ein [**ID3DXPRTEngine**](id3dxprtengine.md) -Objekt, das die PRT-Simulationen (preberechnete Strahlen Übertragung) einer 3D-Szene effizient generieren kann.</span><span class="sxs-lookup"><span data-stu-id="95f1e-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f1e-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="95f1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f1e-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95f1e-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f1e-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="95f1e-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="95f1e-109">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt, das die 3D-Szene modelliert.</span><span class="sxs-lookup"><span data-stu-id="95f1e-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="95f1e-110">Dieses Mesh muss über eine Attribut Tabelle verfügen, in der Vertices in einem eindeutigen Attribut enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="95f1e-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="95f1e-111">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95f1e-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f1e-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="95f1e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="95f1e-113">Optionaler Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit angrenzenden Gesichts Indizes aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95f1e-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="95f1e-114">Die Anzahl der Bytes in diesem Array muss mindestens ((3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)) betragen.</span><span class="sxs-lookup"><span data-stu-id="95f1e-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="95f1e-115">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="95f1e-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95f1e-116">*Extractuvs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95f1e-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f1e-117">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95f1e-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95f1e-118">**True** gibt an, dass Texturen zum Speichern von Albedos-oder PRT-Vektoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95f1e-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="95f1e-119">*pblockermesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95f1e-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f1e-120">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="95f1e-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="95f1e-121">Zeiger auf ein optionales [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, das die 3D-Szene blockiert.</span><span class="sxs-lookup"><span data-stu-id="95f1e-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="95f1e-122">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="95f1e-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95f1e-123">*ppengine* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="95f1e-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95f1e-124">Typ: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="95f1e-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="95f1e-125">Zeiger auf ein Output [**ID3DXPRTEngine**](id3dxprtengine.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="95f1e-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f1e-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95f1e-126">Return value</span></span>

<span data-ttu-id="95f1e-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95f1e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95f1e-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95f1e-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95f1e-129">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="95f1e-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="95f1e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95f1e-130">Remarks</span></span>

<span data-ttu-id="95f1e-131">Verwenden Sie [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) , um mehrere Netzen zu einer einzelnen Gitter Schnittstelle zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="95f1e-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f1e-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95f1e-132">Requirements</span></span>



| <span data-ttu-id="95f1e-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95f1e-133">Requirement</span></span> | <span data-ttu-id="95f1e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="95f1e-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95f1e-135">Header</span><span class="sxs-lookup"><span data-stu-id="95f1e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="95f1e-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="95f1e-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="95f1e-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95f1e-137">Library</span></span><br/> | <dl> <span data-ttu-id="95f1e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95f1e-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95f1e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95f1e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f1e-140">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="95f1e-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
