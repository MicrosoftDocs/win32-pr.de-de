---
description: Verkettet eine Gruppe von Netzen zu einem gemeinsamen Mesh. Diese Methode kann optional eine Matrix Transformation auf jedes Eingabe Mesh und seine Texturkoordinaten anwenden.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: D3DXConcatenateMeshes-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371924"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="8a558-104">D3DXConcatenateMeshes-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a558-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="8a558-105">Verkettet eine Gruppe von Netzen zu einem gemeinsamen Mesh.</span><span class="sxs-lookup"><span data-stu-id="8a558-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="8a558-106">Diese Methode kann optional eine Matrix Transformation auf jedes Eingabe Mesh und seine Texturkoordinaten anwenden.</span><span class="sxs-lookup"><span data-stu-id="8a558-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a558-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a558-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="8a558-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a558-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a558-109">*ppmeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a558-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8a558-111">Array von Eingabe Gitter Zeigern (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="8a558-112">Die Anzahl der Elemente im Array ist nummeshes.</span><span class="sxs-lookup"><span data-stu-id="8a558-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-113">*Nummeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a558-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a558-115">Anzahl der Eingabe-Netzen, die verkettet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a558-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-116">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a558-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a558-118">Gitter Erstellungs Optionen; Dies ist eine Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags.</span><span class="sxs-lookup"><span data-stu-id="8a558-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="8a558-119">Die Gitter Erstellungs Optionen entsprechen dem Optionsparameter, der für [**D3DXCreateMesh**](d3dxcreatemesh.md)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8a558-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a558-120">*pgeomxforms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-121">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a558-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8a558-122">Optionales Array von Geometrie Transformationen.</span><span class="sxs-lookup"><span data-stu-id="8a558-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="8a558-123">Die Anzahl der Elemente im Array ist nummeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="8a558-124">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8a558-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-125">*ptexturexforms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-126">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a558-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8a558-127">Optionales Array von Textur Transformationen.</span><span class="sxs-lookup"><span data-stu-id="8a558-127">Optional array of texture transforms.</span></span> <span data-ttu-id="8a558-128">Die Anzahl der Elemente im Array ist nummeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="8a558-129">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8a558-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-130">*pdecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-131">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a558-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="8a558-132">Optionaler Zeiger auf eine Scheitelpunkt Deklaration (siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="8a558-133">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8a558-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-134">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a558-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-135">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8a558-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8a558-136">Zeiger auf ein [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Gerät, das zum Erstellen des neuen Netzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a558-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8a558-137">*ppmeshout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a558-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a558-138">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a558-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8a558-139">Adresse eines Zeigers auf das erstellte Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a558-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a558-140">Return value</span></span>

<span data-ttu-id="8a558-141">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a558-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a558-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a558-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8a558-143">Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="8a558-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a558-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a558-144">Remarks</span></span>

<span data-ttu-id="8a558-145">Wenn keine [Scheitelpunkt Deklaration](vertex-declaration.md) als Teil des Optionen Gitter Erstellungs-Parameters angegeben wird, generiert die Methode eine Vereinigung aller Scheitelpunkt Deklarationen der Subnetze und fördert ggf. Kanäle und Typen.</span><span class="sxs-lookup"><span data-stu-id="8a558-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="8a558-146">Die-Methode erstellt eine Attribut Tabelle aus Attribut Tabellen der Eingabe-Meshes.</span><span class="sxs-lookup"><span data-stu-id="8a558-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="8a558-147">Um die Erstellung einer Attribut Tabelle sicherzustellen, führen Sie " [**optimieren**](id3dxmesh--optimize.md) " mit Flags aus, die auf D3DXMESHOPT \_ Compact und D3DXMESHOPT \_ attrsort festgelegt sind (siehe [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="8a558-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a558-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a558-148">Requirements</span></span>



| <span data-ttu-id="8a558-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a558-149">Requirement</span></span> | <span data-ttu-id="8a558-150">Wert</span><span class="sxs-lookup"><span data-stu-id="8a558-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a558-151">Header</span><span class="sxs-lookup"><span data-stu-id="8a558-151">Header</span></span><br/>  | <dl> <span data-ttu-id="8a558-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a558-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8a558-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a558-153">Library</span></span><br/> | <dl> <span data-ttu-id="8a558-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a558-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a558-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a558-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a558-156">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8a558-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
