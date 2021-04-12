---
description: Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper:: resampletex-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219632"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="f6847-103">ID3DXTextureGutterHelper:: resampletex-Methode</span><span class="sxs-lookup"><span data-stu-id="f6847-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="f6847-104">Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.</span><span class="sxs-lookup"><span data-stu-id="f6847-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6847-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6847-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="f6847-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6847-107">*ptexturein* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6847-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6847-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f6847-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f6847-109">Textur, die der ursprünglichen Parametrisierung in pmeshin entspricht.</span><span class="sxs-lookup"><span data-stu-id="f6847-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="f6847-110">Diese Textur wird zum Erstellen von ptextureout verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6847-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="f6847-111">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6847-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6847-112">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f6847-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f6847-113">Gitter, das die ursprünglichen und neuen parametrizierungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f6847-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="f6847-114">Die neue Parametrisierung muss in D3DDECLUSAGE \_ texcoord Index 0 gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f6847-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6847-115">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6847-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6847-116">Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="f6847-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="f6847-117">Vertex-Datenverwendung (in Kombination mit usageindex verwendet), die die Komponente der Vertex-Deklaration identifiziert, die die ursprüngliche Parametrisierung in pmeshat enthält.</span><span class="sxs-lookup"><span data-stu-id="f6847-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="f6847-118">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="f6847-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6847-119">Start *Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6847-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6847-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6847-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6847-121">NULL basierter Index (verwendet in Kombination mit der Verwendung), der die Komponente der Vertex-Deklaration identifiziert, die die ursprüngliche Parametrisierung in pmeshat enthält.</span><span class="sxs-lookup"><span data-stu-id="f6847-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="f6847-122">Die Kombination aus D3DDECLUSAGE \_ texcoord und Index 0 ist für die neue Parametrisierung erforderlich. es kann eine beliebige andere Kombination von Verwendung/Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6847-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="f6847-123">*ptextureout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6847-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6847-124">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f6847-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f6847-125">Textur wird erneut entnommen.</span><span class="sxs-lookup"><span data-stu-id="f6847-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6847-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6847-126">Return value</span></span>

<span data-ttu-id="f6847-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6847-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6847-128">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6847-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f6847-129">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="f6847-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6847-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6847-130">Remarks</span></span>

<span data-ttu-id="f6847-131">Bei einer Parametrisierung im Fall dieser Funktion handelt es sich um einen Satz von Texturkoordinaten, der die Dreiecke eines Netzes den Dreiecken einer Textur zuordnet.</span><span class="sxs-lookup"><span data-stu-id="f6847-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="f6847-132">Die neue Parametrisierung ist der Satz von Texturkoordinaten, der in der bundbundhilfsschnittstelle enthalten ist, und die ursprüngliche Parametrisierung ist der Satz von Texturkoordinaten, der im Eingabe Mesh enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f6847-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="f6847-133">Es wird davon ausgegangen, dass die Texturkoordinaten zwischen 0 und 1 (einschließlich) liegen, und die neue Parametrisierung muss in der Scheitelpunkt Deklaration als Texturkoordinaten Index 0 deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="f6847-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="f6847-134">Die ursprüngliche Textur und die neu komprimierte Textur müssen dieselbe Breite und Höhe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f6847-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="f6847-135">So bereiten Sie z. b. die Neuerstellung einer Textur vor:</span><span class="sxs-lookup"><span data-stu-id="f6847-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="f6847-136">Erstellen Sie die ursprüngliche Textur Schnittstelle (poriginaltex unten), indem Sie eine Funktion wie [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6847-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="f6847-137">Erstellen Sie die neue Textur Schnittstelle für die neu komprimierte Textur (presampledtex unten).</span><span class="sxs-lookup"><span data-stu-id="f6847-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="f6847-138">Die Größe dieser Textur muss mit der Größe (Breite und Höhe) der Struktur des bundstehilfsobjekts identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f6847-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="f6847-139">Rufen Sie [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) auf, um die neue Parametrisierung zu erhalten, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f6847-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="f6847-140">Ein häufiges Szenario ist die Verwendung von uvatlas zum Erstellen eines Textur Atlas und die anschließende erneute Stichprobe der Textur mithilfe von resampletex in die neue Parametrisierung.</span><span class="sxs-lookup"><span data-stu-id="f6847-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="f6847-141">Weitere Informationen zu Atlases finden Sie unter [Verwenden von uvatlas (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="f6847-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6847-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6847-142">Requirements</span></span>



| <span data-ttu-id="f6847-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6847-143">Requirement</span></span> | <span data-ttu-id="f6847-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f6847-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6847-145">Header</span><span class="sxs-lookup"><span data-stu-id="f6847-145">Header</span></span><br/>  | <dl> <span data-ttu-id="f6847-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6847-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f6847-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6847-147">Library</span></span><br/> | <dl> <span data-ttu-id="f6847-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6847-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6847-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6847-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6847-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f6847-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="f6847-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="f6847-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
