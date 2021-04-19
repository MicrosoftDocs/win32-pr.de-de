---
description: Speichert ein Mesh in einer x-Datei.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: D3DXSaveMeshToX-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361199"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="e1fa9-103">D3DXSaveMeshToX-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1fa9-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="e1fa9-104">Speichert ein Mesh in einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fa9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1fa9-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="e1fa9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1fa9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1fa9-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1fa9-109">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="e1fa9-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e1fa9-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e1fa9-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-113">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-114">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="e1fa9-115">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das Mesh darstellt, das in einer x-Datei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-116">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-117">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1fa9-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e1fa9-118">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e1fa9-119">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-120">*pmaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-121">Typ: **Konstanten [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1fa9-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="e1fa9-122">Ein Zeiger auf ein Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen, die Material Informationen enthalten, die in der x-Datei gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-123">" *Peer-ectinhaltungen* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-124">Typ: **Konstanten [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1fa9-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="e1fa9-125">Zeiger auf ein Array von Effekt Instanzen, eines pro Attribut Gruppe im Mesh.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="e1fa9-126">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="e1fa9-127">Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="e1fa9-128">Weitere Informationen finden Sie unter [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="e1fa9-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-129">*Nummaterial* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1fa9-131">Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *pmaterials* -Array.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa9-132">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1fa9-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa9-133">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1fa9-134">Eine Kombination aus Dateiformat und Speicheroptionen beim Speichern einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="e1fa9-135">Siehe [D3DX X-Datei Konstanten](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e1fa9-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1fa9-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1fa9-136">Return value</span></span>

<span data-ttu-id="e1fa9-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1fa9-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e1fa9-139">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1fa9-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1fa9-140">Remarks</span></span>

<span data-ttu-id="e1fa9-141">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e1fa9-142">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveMeshToXW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="e1fa9-143">Andernfalls wird der Funktions Aufruhe in D3DXSaveMeshToXA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="e1fa9-144">Das Standarddatei Format ist Binary. Wenn eine Datei jedoch sowohl als binäre als auch als Textdatei angegeben wird, wird Sie als Textdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="e1fa9-145">Unabhängig vom Dateiformat können Sie auch das komprimierte Format verwenden, um die Dateigröße zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="e1fa9-146">Im folgenden finden Sie ein typisches Codebeispiel für die Verwendung dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1fa9-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="e1fa9-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1fa9-147">Requirements</span></span>



| <span data-ttu-id="e1fa9-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1fa9-148">Requirement</span></span> | <span data-ttu-id="e1fa9-149">Wert</span><span class="sxs-lookup"><span data-stu-id="e1fa9-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fa9-150">Header</span><span class="sxs-lookup"><span data-stu-id="e1fa9-150">Header</span></span><br/>  | <dl> <span data-ttu-id="e1fa9-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa9-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e1fa9-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1fa9-152">Library</span></span><br/> | <dl> <span data-ttu-id="e1fa9-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa9-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1fa9-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1fa9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fa9-155">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e1fa9-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="e1fa9-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="e1fa9-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e1fa9-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
