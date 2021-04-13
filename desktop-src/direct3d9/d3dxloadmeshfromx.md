---
description: Lädt ein Mesh aus einer DirectX. x-Datei.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: D3DXLoadMeshFromX-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354806"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="90ca1-103">D3DXLoadMeshFromX-Funktion</span><span class="sxs-lookup"><span data-stu-id="90ca1-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="90ca1-104">Lädt ein Mesh aus einer DirectX. x-Datei.</span><span class="sxs-lookup"><span data-stu-id="90ca1-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ca1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90ca1-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="90ca1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ca1-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90ca1-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90ca1-109">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="90ca1-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="90ca1-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="90ca1-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="90ca1-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="90ca1-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="90ca1-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-113">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90ca1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90ca1-115">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-116">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-117">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="90ca1-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="90ca1-118">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-119">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-120">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="90ca1-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="90ca1-121">Zeiger auf einen Puffer, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="90ca1-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="90ca1-122">Die Daten der Daten enthalten ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="90ca1-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="90ca1-123">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="90ca1-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-124">*ppmaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="90ca1-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="90ca1-126">Zeiger auf einen Puffer, der Materialdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="90ca1-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="90ca1-127">Der Puffer enthält ein Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen, das Informationen aus der DirectX-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="90ca1-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="90ca1-128">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="90ca1-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-129">*ppeer-ectinhaltungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="90ca1-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="90ca1-131">Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="90ca1-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="90ca1-132">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ca1-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="90ca1-133">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="90ca1-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="90ca1-134">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="90ca1-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-135">*pnummaterials* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-136">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90ca1-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90ca1-137">Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="90ca1-138">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90ca1-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ca1-139">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="90ca1-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="90ca1-140">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ca1-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90ca1-141">Return value</span></span>

<span data-ttu-id="90ca1-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90ca1-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90ca1-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90ca1-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="90ca1-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="90ca1-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ca1-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90ca1-145">Remarks</span></span>

<span data-ttu-id="90ca1-146">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="90ca1-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="90ca1-147">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadMeshFromXW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="90ca1-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="90ca1-148">Andernfalls wird der Funktions Aufruhe in D3DXLoadMeshFromXA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ca1-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="90ca1-149">Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert.</span><span class="sxs-lookup"><span data-stu-id="90ca1-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="90ca1-150">Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.</span><span class="sxs-lookup"><span data-stu-id="90ca1-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="90ca1-151">Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="90ca1-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="90ca1-152">Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.</span><span class="sxs-lookup"><span data-stu-id="90ca1-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="90ca1-153">Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="90ca1-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="90ca1-154">Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name".</span><span class="sxs-lookup"><span data-stu-id="90ca1-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="90ca1-155">Diese enthält den Namen der Zeichen folgen Datei für die Textur.</span><span class="sxs-lookup"><span data-stu-id="90ca1-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ca1-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90ca1-156">Requirements</span></span>



| <span data-ttu-id="90ca1-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90ca1-157">Requirement</span></span> | <span data-ttu-id="90ca1-158">Wert</span><span class="sxs-lookup"><span data-stu-id="90ca1-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90ca1-159">Header</span><span class="sxs-lookup"><span data-stu-id="90ca1-159">Header</span></span><br/>  | <dl> <span data-ttu-id="90ca1-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ca1-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="90ca1-161">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90ca1-161">Library</span></span><br/> | <dl> <span data-ttu-id="90ca1-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90ca1-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90ca1-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90ca1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ca1-164">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="90ca1-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="90ca1-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="90ca1-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="90ca1-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="90ca1-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
