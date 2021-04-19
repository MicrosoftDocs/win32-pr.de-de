---
description: Ruft Mesh-Geometrie-Verschiebungs Parameter ab.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh:: getverdräneparam-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369342"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="9d430-103">ID3DXPatchMesh:: getverdräneparam-Methode</span><span class="sxs-lookup"><span data-stu-id="9d430-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="9d430-104">Ruft Mesh-Geometrie-Verschiebungs Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="9d430-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d430-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d430-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="9d430-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d430-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d430-107">*Textur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-108">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="9d430-109">Textur, die die Verschiebungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9d430-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="9d430-110">*MinFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-111">Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="9d430-112">Minizierungsebene.</span><span class="sxs-lookup"><span data-stu-id="9d430-112">Minification level.</span></span> <span data-ttu-id="9d430-113">Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9d430-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d430-114">*MagFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-115">Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="9d430-116">Vergrößerungs Stufe.</span><span class="sxs-lookup"><span data-stu-id="9d430-116">Magnification level.</span></span> <span data-ttu-id="9d430-117">Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9d430-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d430-118">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-119">Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="9d430-120">MIP-Filter Ebene.</span><span class="sxs-lookup"><span data-stu-id="9d430-120">Mip filter level.</span></span> <span data-ttu-id="9d430-121">Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9d430-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d430-122"> Umbruch \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-123">Typ: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="9d430-124">Der Textur Adress Umbruch Modus.</span><span class="sxs-lookup"><span data-stu-id="9d430-124">Texture address wrap mode.</span></span> <span data-ttu-id="9d430-125">Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="9d430-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d430-126">*dwlodbias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d430-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d430-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d430-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d430-128">Grad des Detail-Bias-Werts.</span><span class="sxs-lookup"><span data-stu-id="9d430-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d430-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d430-129">Return value</span></span>

<span data-ttu-id="9d430-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d430-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d430-131">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9d430-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9d430-132">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="9d430-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d430-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d430-133">Remarks</span></span>

<span data-ttu-id="9d430-134">Verschiebungs Zuordnungen können nur 2D-Texturen sein.</span><span class="sxs-lookup"><span data-stu-id="9d430-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="9d430-135">Mipmapping wird für nicht Adaptive Mosaik ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9d430-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d430-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d430-136">Requirements</span></span>



| <span data-ttu-id="9d430-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d430-137">Requirement</span></span> | <span data-ttu-id="9d430-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9d430-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d430-139">Header</span><span class="sxs-lookup"><span data-stu-id="9d430-139">Header</span></span><br/>  | <dl> <span data-ttu-id="9d430-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d430-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9d430-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d430-141">Library</span></span><br/> | <dl> <span data-ttu-id="9d430-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d430-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d430-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d430-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d430-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="9d430-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
