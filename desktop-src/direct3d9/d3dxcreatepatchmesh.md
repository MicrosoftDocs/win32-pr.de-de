---
description: Erstellt ein Mesh aus einem Steuerelement patchmesh.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: D3DXCreatePatchMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355857"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="7eb8c-103">D3DXCreatePatchMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="7eb8c-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="7eb8c-104">Erstellt ein Mesh aus einem Steuerelement patchmesh.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eb8c-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="7eb8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7eb8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb8c-107">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-108">Typ: **Konstanten [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="7eb8c-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="7eb8c-109">Struktur der Patchinformationen.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-109">Patch information structure.</span></span> <span data-ttu-id="7eb8c-110">Weitere Informationen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="7eb8c-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-111">*dwnumpatches* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7eb8c-113">Anzahl der Patches.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-114">*dwnumvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7eb8c-116">Anzahl der Steuerungs Scheitel Punkte im Patch.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-117">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-118">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7eb8c-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-119">Unused.</span></span> <span data-ttu-id="7eb8c-120">Reserviert für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-121">*pdecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-122">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="7eb8c-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="7eb8c-123">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-124">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-125">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7eb8c-126">Zeiger auf das Gerät, das das patchmesh erstellt.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="7eb8c-127">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="7eb8c-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="7eb8c-128">*ppatchmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7eb8c-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb8c-129">Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7eb8c-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="7eb8c-130">Zeiger auf das [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Objekt, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb8c-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7eb8c-131">Return value</span></span>

<span data-ttu-id="7eb8c-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7eb8c-133">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7eb8c-134">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eb8c-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7eb8c-135">Remarks</span></span>

<span data-ttu-id="7eb8c-136">Diese Methode nimmt ein eingaberpatchmesh an und konvertiert es in ein Mosaik Gitter.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="7eb8c-137">Patchnetze verwenden 16-Bit-Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="7eb8c-138">Daher sind Indizes zu [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="7eb8c-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb8c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7eb8c-139">Requirements</span></span>



| <span data-ttu-id="7eb8c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eb8c-140">Requirement</span></span> | <span data-ttu-id="7eb8c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="7eb8c-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb8c-142">Header</span><span class="sxs-lookup"><span data-stu-id="7eb8c-142">Header</span></span><br/>  | <dl> <span data-ttu-id="7eb8c-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eb8c-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7eb8c-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7eb8c-144">Library</span></span><br/> | <dl> <span data-ttu-id="7eb8c-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eb8c-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7eb8c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eb8c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb8c-147">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7eb8c-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7eb8c-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="7eb8c-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
