---
description: Berechnet das pro-Dreieck-IMT aus einer Textur, die einem Mesh zugeordnet ist, um optional als Eingabe für die D3DX uvatlas-Funktionen verwendet zu werden.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: D3DXComputeIMTFromTexture-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050906"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="9ea81-103">D3DXComputeIMTFromTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="9ea81-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="9ea81-104">Berechnet das pro-Dreieck-IMT aus einer Textur, die einem Mesh zugeordnet ist, um optional als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="9ea81-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ea81-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="9ea81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ea81-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ea81-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea81-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9ea81-109">Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.</span><span class="sxs-lookup"><span data-stu-id="9ea81-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-110">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ea81-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea81-111">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="9ea81-112">Ein Zeiger auf die Textur (siehe [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)), die dem Mesh zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9ea81-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-113">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ea81-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea81-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ea81-115">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea81-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-116">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ea81-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea81-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ea81-118">Textur Umbruch Optionen.</span><span class="sxs-lookup"><span data-stu-id="9ea81-118">Texture wrap options.</span></span> <span data-ttu-id="9ea81-119">Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ea81-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-120">*pstatus Callback*</span><span class="sxs-lookup"><span data-stu-id="9ea81-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea81-121">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="9ea81-122">Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="9ea81-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-123">*pusercontext*</span><span class="sxs-lookup"><span data-stu-id="9ea81-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea81-124">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ea81-125">Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="9ea81-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="9ea81-126">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9ea81-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="9ea81-127">*ppimtdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ea81-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea81-128">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ea81-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9ea81-129">Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="9ea81-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="9ea81-130">Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="9ea81-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ea81-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ea81-131">Return value</span></span>

<span data-ttu-id="9ea81-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ea81-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ea81-133">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="9ea81-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea81-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ea81-134">Remarks</span></span>

<span data-ttu-id="9ea81-135">Wenn eine Textur über der Oberfläche des Mesh zugeordnet ist, berechnet der Algorithmus den IMT für jedes Gesicht.</span><span class="sxs-lookup"><span data-stu-id="9ea81-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="9ea81-136">Dies führt dazu, dass Dreiecke, die Signaldaten niedriger Frequenz enthalten, bei der Parametrisierung mit den uvatlas-Funktionen weniger Speicherplatz im endgültigen Textur Atlas benötigt.</span><span class="sxs-lookup"><span data-stu-id="9ea81-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="9ea81-137">Es wird davon ausgegangen, dass die Textur über das Mesh bilinear interpoliert wird.</span><span class="sxs-lookup"><span data-stu-id="9ea81-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea81-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ea81-138">Requirements</span></span>



| <span data-ttu-id="9ea81-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ea81-139">Requirement</span></span> | <span data-ttu-id="9ea81-140">Wert</span><span class="sxs-lookup"><span data-stu-id="9ea81-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea81-141">Header</span><span class="sxs-lookup"><span data-stu-id="9ea81-141">Header</span></span><br/>  | <dl> <span data-ttu-id="9ea81-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ea81-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9ea81-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ea81-143">Library</span></span><br/> | <dl> <span data-ttu-id="9ea81-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ea81-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ea81-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ea81-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea81-146">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9ea81-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="9ea81-147">Verwenden von uvatlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9ea81-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
