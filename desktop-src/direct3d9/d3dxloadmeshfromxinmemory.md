---
description: Lädt ein Mesh aus dem Arbeitsspeicher.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: D3DXLoadMeshFromXInMemory-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373511"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="9b334-103">D3DXLoadMeshFromXInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="9b334-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="9b334-104">Lädt ein Mesh aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9b334-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b334-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b334-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9b334-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b334-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b334-107">Arbeits *Speicher* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b334-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b334-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b334-109">Zeiger auf den Arbeitsspeicher Puffer, der die Mesh-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9b334-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-110">*Sizeofmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b334-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b334-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b334-112">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9b334-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-113">*Optionen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b334-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b334-115">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="9b334-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-116">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b334-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-117">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9b334-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9b334-118">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b334-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-119">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-120">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b334-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b334-121">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b334-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="9b334-122">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="9b334-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-123">*ppmaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-124">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b334-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b334-125">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b334-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="9b334-126">Wenn diese Methode zurückgegeben wird, wird dieser Parameter mit einem Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen gefüllt, das Informationen enthält, die in der DirectX-Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9b334-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-127">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-128">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b334-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b334-129">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="9b334-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="9b334-130">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b334-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="9b334-131">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="9b334-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="9b334-132">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9b334-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b334-133">*pnummaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b334-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b334-135">Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9b334-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="9b334-136">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b334-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b334-137">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b334-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9b334-138">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b334-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b334-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b334-139">Return value</span></span>

<span data-ttu-id="9b334-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b334-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b334-141">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9b334-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b334-142">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="9b334-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b334-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b334-143">Remarks</span></span>

<span data-ttu-id="9b334-144">Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert.</span><span class="sxs-lookup"><span data-stu-id="9b334-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="9b334-145">Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.</span><span class="sxs-lookup"><span data-stu-id="9b334-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="9b334-146">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9b334-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="9b334-147">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b334-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="9b334-148">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b334-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="9b334-149">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="9b334-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="9b334-150">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="9b334-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b334-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b334-151">Requirements</span></span>



| <span data-ttu-id="9b334-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b334-152">Requirement</span></span> | <span data-ttu-id="9b334-153">Wert</span><span class="sxs-lookup"><span data-stu-id="9b334-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b334-154">Header</span><span class="sxs-lookup"><span data-stu-id="9b334-154">Header</span></span><br/>  | <dl> <span data-ttu-id="9b334-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b334-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9b334-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b334-156">Library</span></span><br/> | <dl> <span data-ttu-id="9b334-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b334-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b334-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b334-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b334-159">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9b334-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="9b334-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9b334-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="9b334-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="9b334-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
