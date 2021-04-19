---
description: Konvertiert die angegebene Gitter Teilmenge in einen einzelnen Dreieck Streifen.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357230"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="a32d4-103">D3DXConvertMeshSubsetToSingleStrip-Funktion</span><span class="sxs-lookup"><span data-stu-id="a32d4-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="a32d4-104">Konvertiert die angegebene Gitter Teilmenge in einen einzelnen Dreieck Streifen.</span><span class="sxs-lookup"><span data-stu-id="a32d4-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32d4-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="a32d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32d4-107">*Mesda* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a32d4-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a32d4-108">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a32d4-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="a32d4-109">Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das Mesh darstellt, das in einen Strip konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a32d4-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="a32d4-110">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a32d4-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a32d4-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a32d4-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a32d4-112">Attribut-ID der Mesh-Teilmenge, die in Striche konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a32d4-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="a32d4-113">*Iboptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a32d4-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a32d4-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a32d4-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a32d4-115">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Optionen zum Erstellen des Index Puffers angeben.</span><span class="sxs-lookup"><span data-stu-id="a32d4-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="a32d4-116">Darf nicht D3DXMESH \_ 32 Bit sein.</span><span class="sxs-lookup"><span data-stu-id="a32d4-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="a32d4-117">Der Index Puffer wird mit 32-Bit-oder 16-Bit-Indizes erstellt, abhängig vom Format des Index Puffers des Netzes, das durch den *mesda* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32d4-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a32d4-118">*ppindexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a32d4-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a32d4-119">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="a32d4-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="a32d4-120">Ein Zeiger auf eine [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle, die den Index Puffer darstellt, der den Strip enthält.</span><span class="sxs-lookup"><span data-stu-id="a32d4-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="a32d4-121">*pnumindizes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a32d4-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a32d4-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a32d4-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a32d4-123">Anzahl der Indizes im Puffer, die im *ppindexbuffer* -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a32d4-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32d4-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a32d4-124">Return value</span></span>

<span data-ttu-id="a32d4-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a32d4-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a32d4-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a32d4-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a32d4-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="a32d4-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32d4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a32d4-128">Remarks</span></span>

<span data-ttu-id="a32d4-129">Stellen Sie vor dem Ausführen dieser Funktion " [**optimieren**](id3dxmesh--optimize.md) " oder " [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)" mit dem D3DXMESHOPT \_ attrsort-Flag her.</span><span class="sxs-lookup"><span data-stu-id="a32d4-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32d4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a32d4-130">Requirements</span></span>



| <span data-ttu-id="a32d4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a32d4-131">Requirement</span></span> | <span data-ttu-id="a32d4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a32d4-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a32d4-133">Header</span><span class="sxs-lookup"><span data-stu-id="a32d4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a32d4-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a32d4-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a32d4-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a32d4-135">Library</span></span><br/> | <dl> <span data-ttu-id="a32d4-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a32d4-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a32d4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a32d4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32d4-138">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a32d4-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
