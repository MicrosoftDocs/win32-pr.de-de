---
description: Lädt ein Skin-Mesh aus einem DirectX. x-Datei Datenobjekt.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: D3DXLoadSkinMeshFromXof-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761949"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="95b15-103">D3DXLoadSkinMeshFromXof-Funktion</span><span class="sxs-lookup"><span data-stu-id="95b15-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="95b15-104">Lädt ein Skin-Mesh aus einem DirectX. x-Datei Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="95b15-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b15-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="95b15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95b15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b15-107">*pxofmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b15-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-108">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="95b15-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="95b15-109">Zeiger auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zu ladende Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="95b15-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-110">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b15-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b15-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b15-112">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="95b15-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-113">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b15-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-114">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="95b15-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="95b15-115">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="95b15-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-116">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-117">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="95b15-118">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="95b15-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="95b15-119">Wenn diese Methode zurückgegeben wird, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="95b15-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-120">*ppmaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-121">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="95b15-122">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="95b15-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="95b15-123">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen gefüllt.</span><span class="sxs-lookup"><span data-stu-id="95b15-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-124">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="95b15-126">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="95b15-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="95b15-127">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95b15-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="95b15-128">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="95b15-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="95b15-129">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="95b15-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="95b15-130">*pmatout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="95b15-132">Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="95b15-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-133">*ppskininfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-134">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="95b15-135">Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die die Skinning-Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="95b15-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="95b15-136">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95b15-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b15-137">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="95b15-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="95b15-138">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="95b15-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b15-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95b15-139">Return value</span></span>

<span data-ttu-id="95b15-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95b15-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95b15-141">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95b15-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95b15-142">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory</span><span class="sxs-lookup"><span data-stu-id="95b15-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="95b15-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b15-143">Remarks</span></span>

<span data-ttu-id="95b15-144">Diese Methode nimmt einen Zeiger auf ein internes Objekt in der x-Datei an, sodass Sie die Frame Hierarchie laden können.</span><span class="sxs-lookup"><span data-stu-id="95b15-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="95b15-145">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="95b15-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="95b15-146">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="95b15-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="95b15-147">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="95b15-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="95b15-148">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="95b15-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="95b15-149">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="95b15-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b15-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95b15-150">Requirements</span></span>



| <span data-ttu-id="95b15-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b15-151">Requirement</span></span> | <span data-ttu-id="95b15-152">Wert</span><span class="sxs-lookup"><span data-stu-id="95b15-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95b15-153">Header</span><span class="sxs-lookup"><span data-stu-id="95b15-153">Header</span></span><br/>  | <dl> <span data-ttu-id="95b15-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b15-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="95b15-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95b15-155">Library</span></span><br/> | <dl> <span data-ttu-id="95b15-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95b15-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95b15-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b15-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b15-158">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="95b15-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="95b15-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="95b15-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="95b15-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="95b15-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
