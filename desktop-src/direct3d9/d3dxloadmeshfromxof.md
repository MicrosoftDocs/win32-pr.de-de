---
description: Lädt ein Mesh aus einem ID3DXFileData-Objekt.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: D3DXLoadMeshFromXof-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354797"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="cd73a-103">D3DXLoadMeshFromXof-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd73a-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="cd73a-104">Lädt ein Mesh aus einem [**ID3DXFileData**](id3dxfiledata.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd73a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd73a-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="cd73a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd73a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd73a-107">*pxofmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-108">Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="cd73a-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="cd73a-109">Zeiger auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zu ladende Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-110">*Optionen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd73a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd73a-112">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-114">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cd73a-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cd73a-115">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-116">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-117">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd73a-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cd73a-118">Zeiger auf einen Puffer, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="cd73a-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="cd73a-119">Die Daten der Daten enthalten ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="cd73a-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="cd73a-120">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cd73a-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-121">*ppmaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-122">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd73a-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cd73a-123">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cd73a-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="cd73a-124">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen gefüllt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-125">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-126">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd73a-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cd73a-127">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="cd73a-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="cd73a-128">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd73a-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="cd73a-129">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="cd73a-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="cd73a-130">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cd73a-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-131">*pnummaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd73a-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd73a-133">Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="cd73a-134">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd73a-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd73a-135">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd73a-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cd73a-136">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd73a-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd73a-137">Return value</span></span>

<span data-ttu-id="cd73a-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd73a-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd73a-139">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd73a-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd73a-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="cd73a-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd73a-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd73a-141">Remarks</span></span>

<span data-ttu-id="cd73a-142">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="cd73a-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="cd73a-143">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cd73a-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="cd73a-144">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="cd73a-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="cd73a-145">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="cd73a-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="cd73a-146">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="cd73a-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd73a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd73a-147">Requirements</span></span>



| <span data-ttu-id="cd73a-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd73a-148">Requirement</span></span> | <span data-ttu-id="cd73a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="cd73a-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd73a-150">Header</span><span class="sxs-lookup"><span data-stu-id="cd73a-150">Header</span></span><br/>  | <dl> <span data-ttu-id="cd73a-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd73a-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cd73a-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd73a-152">Library</span></span><br/> | <dl> <span data-ttu-id="cd73a-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd73a-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd73a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd73a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd73a-155">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cd73a-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="cd73a-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd73a-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="cd73a-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="cd73a-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
