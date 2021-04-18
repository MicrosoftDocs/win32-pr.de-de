---
description: Lädt ein patchmesh aus einem ID3DXFileData-Objekt.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: D3DXLoadPatchMeshFromXof-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365081"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="12a86-103">D3DXLoadPatchMeshFromXof-Funktion</span><span class="sxs-lookup"><span data-stu-id="12a86-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="12a86-104">Lädt ein patchmesh aus einem [**ID3DXFileData**](id3dxfiledata.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="12a86-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a86-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="12a86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a86-107">*pxofmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a86-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-108">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="12a86-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="12a86-109">Zeiger auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zu ladende Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="12a86-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="12a86-110">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a86-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12a86-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12a86-112">Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags, die Erstellungs Optionen für das Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="12a86-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="12a86-113">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a86-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-114">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="12a86-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="12a86-115">Zeiger auf das Gerät, aus dem das Mesh erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="12a86-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="12a86-116">*ppmaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12a86-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-117">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="12a86-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="12a86-118">Ein Array von Materialien, das im Mesh enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="12a86-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="12a86-119">Jedes Material wird von einer [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle indiziert.</span><span class="sxs-lookup"><span data-stu-id="12a86-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="12a86-120">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12a86-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-121">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="12a86-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="12a86-122">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="12a86-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="12a86-123">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12a86-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="12a86-124">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="12a86-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="12a86-125">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="12a86-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="12a86-126">*pnummaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12a86-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-127">Type: **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="12a86-127">Type: **PDWORD**</span></span>

<span data-ttu-id="12a86-128">Ein Zeiger, der die Anzahl der Materialien im Mesh enthält.</span><span class="sxs-lookup"><span data-stu-id="12a86-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="12a86-129">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12a86-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a86-130">Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="12a86-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="12a86-131">Adresse eines Zeigers auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="12a86-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a86-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12a86-132">Return value</span></span>

<span data-ttu-id="12a86-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12a86-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12a86-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12a86-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="12a86-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="12a86-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="12a86-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12a86-136">Remarks</span></span>

<span data-ttu-id="12a86-137">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="12a86-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="12a86-138">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="12a86-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="12a86-139">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="12a86-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="12a86-140">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="12a86-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="12a86-141">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="12a86-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a86-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12a86-142">Requirements</span></span>



| <span data-ttu-id="12a86-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12a86-143">Requirement</span></span> | <span data-ttu-id="12a86-144">Wert</span><span class="sxs-lookup"><span data-stu-id="12a86-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12a86-145">Header</span><span class="sxs-lookup"><span data-stu-id="12a86-145">Header</span></span><br/>  | <dl> <span data-ttu-id="12a86-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a86-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="12a86-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12a86-147">Library</span></span><br/> | <dl> <span data-ttu-id="12a86-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12a86-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12a86-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12a86-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a86-150">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="12a86-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="12a86-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="12a86-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="12a86-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="12a86-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
