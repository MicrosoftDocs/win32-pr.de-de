---
description: Konvertiert die angegebene Gitter Teilmenge in eine Reihe von Bändern.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: D3DXConvertMeshSubsetToStrips-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353396"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="64f0c-103">D3DXConvertMeshSubsetToStrips-Funktion</span><span class="sxs-lookup"><span data-stu-id="64f0c-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="64f0c-104">Konvertiert die angegebene Gitter Teilmenge in eine Reihe von Bändern.</span><span class="sxs-lookup"><span data-stu-id="64f0c-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f0c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f0c-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="64f0c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f0c-107">*Mesda* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-108">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="64f0c-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="64f0c-109">Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das Mesh darstellt, das in einen Strip konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f0c-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-110">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64f0c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64f0c-112">Attribut-ID der Mesh-Teilmenge, die in Striche konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f0c-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-113">*Iboptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64f0c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64f0c-115">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Optionen zum Erstellen des Index Puffers angeben.</span><span class="sxs-lookup"><span data-stu-id="64f0c-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="64f0c-116">Darf nicht D3DXMESH \_ 32 Bit sein.</span><span class="sxs-lookup"><span data-stu-id="64f0c-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="64f0c-117">Der Index Puffer wird mit 32-Bit-oder 16-Bit-Indizes erstellt, abhängig vom Format des Index Puffers des Netzes, das durch den *mesda* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64f0c-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-118">*ppindexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-119">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="64f0c-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="64f0c-120">Zeiger auf eine [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle, die den Index Puffer darstellt, der den Strip enthält.</span><span class="sxs-lookup"><span data-stu-id="64f0c-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-121">*pnumindizes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="64f0c-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="64f0c-123">Anzahl der Indizes im Puffer, die im *ppindexbuffer* -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64f0c-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-124">*ppstriplengths* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64f0c-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64f0c-126">Ein Puffer, der ein Array von einem DWORD pro Strip enthält, das die Anzahl der Dreiecke in diesem Strip angibt.</span><span class="sxs-lookup"><span data-stu-id="64f0c-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="64f0c-127">*pnumstrips* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f0c-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0c-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="64f0c-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="64f0c-129">Die Anzahl einzelner Bänder im Index Puffer und das entsprechende Strip-Längen Array.</span><span class="sxs-lookup"><span data-stu-id="64f0c-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f0c-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f0c-130">Return value</span></span>

<span data-ttu-id="64f0c-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64f0c-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64f0c-132">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64f0c-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64f0c-133">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="64f0c-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f0c-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f0c-134">Remarks</span></span>

<span data-ttu-id="64f0c-135">Stellen Sie vor dem Ausführen dieser Funktion " [**optimieren**](id3dxmesh--optimize.md) " oder " [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)" mit dem D3DXMESHOPT \_ attrsort-Flag her.</span><span class="sxs-lookup"><span data-stu-id="64f0c-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f0c-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f0c-136">Requirements</span></span>



| <span data-ttu-id="64f0c-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f0c-137">Requirement</span></span> | <span data-ttu-id="64f0c-138">Wert</span><span class="sxs-lookup"><span data-stu-id="64f0c-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64f0c-139">Header</span><span class="sxs-lookup"><span data-stu-id="64f0c-139">Header</span></span><br/>  | <dl> <span data-ttu-id="64f0c-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f0c-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="64f0c-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64f0c-141">Library</span></span><br/> | <dl> <span data-ttu-id="64f0c-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64f0c-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64f0c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f0c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f0c-144">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="64f0c-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
