---
description: Lädt ein Mesh aus einer Ressource.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: D3DXLoadMeshFromXResource-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762030"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="5a87f-103">D3DXLoadMeshFromXResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="5a87f-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="5a87f-104">Lädt ein Mesh aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a87f-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a87f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a87f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="5a87f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a87f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a87f-107">*Modul* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a87f-109">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, das zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5a87f-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="5a87f-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5a87f-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-111">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a87f-113">Ein Zeiger auf eine Zeichenfolge, die die Ressource angibt, aus der das Mesh erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a87f-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="5a87f-114">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5a87f-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-115">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-116">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a87f-117">Zeiger auf eine Zeichenfolge, die den Ressourcentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="5a87f-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="5a87f-118">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5a87f-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-119">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a87f-121">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="5a87f-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-122">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-123">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5a87f-124">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="5a87f-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-125">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-126">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a87f-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a87f-127">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a87f-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="5a87f-128">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="5a87f-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-129">*ppmaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a87f-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a87f-131">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a87f-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="5a87f-132">Wenn diese Methode zurückgegeben wird, wird dieser Parameter mit einem Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen gefüllt, das Informationen enthält, die in der DirectX-Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5a87f-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-133">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-134">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a87f-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a87f-135">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="5a87f-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="5a87f-136">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a87f-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="5a87f-137">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="5a87f-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="5a87f-138">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5a87f-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-139">*pnummaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-140">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a87f-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a87f-141">Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5a87f-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="5a87f-142">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a87f-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a87f-143">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a87f-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="5a87f-144">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a87f-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a87f-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a87f-145">Return value</span></span>

<span data-ttu-id="5a87f-146">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a87f-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a87f-147">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a87f-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a87f-148">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="5a87f-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a87f-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a87f-149">Remarks</span></span>

<span data-ttu-id="5a87f-150">Weitere Informationen zu Modul-, namens-und Typparametern finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="5a87f-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="5a87f-151">Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert.</span><span class="sxs-lookup"><span data-stu-id="5a87f-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="5a87f-152">Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.</span><span class="sxs-lookup"><span data-stu-id="5a87f-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="5a87f-153">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="5a87f-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="5a87f-154">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5a87f-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="5a87f-155">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="5a87f-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="5a87f-156">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="5a87f-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="5a87f-157">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="5a87f-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a87f-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a87f-158">Requirements</span></span>



| <span data-ttu-id="5a87f-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a87f-159">Requirement</span></span> | <span data-ttu-id="5a87f-160">Wert</span><span class="sxs-lookup"><span data-stu-id="5a87f-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a87f-161">Header</span><span class="sxs-lookup"><span data-stu-id="5a87f-161">Header</span></span><br/>  | <dl> <span data-ttu-id="5a87f-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a87f-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5a87f-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a87f-163">Library</span></span><br/> | <dl> <span data-ttu-id="5a87f-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a87f-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a87f-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a87f-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a87f-166">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5a87f-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="5a87f-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5a87f-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="5a87f-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="5a87f-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
