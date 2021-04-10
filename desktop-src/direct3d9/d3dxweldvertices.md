---
description: Führt eine kombinieren von replizierten Vertices mit identischen Attributen aus. Diese Methode verwendet angegebene Epsilon-Werte für Gleichheits Vergleiche.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: D3DXWeldVertices-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762084"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="037ea-104">D3DXWeldVertices-Funktion</span><span class="sxs-lookup"><span data-stu-id="037ea-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="037ea-105">Führt eine kombinieren von replizierten Vertices mit identischen Attributen aus.</span><span class="sxs-lookup"><span data-stu-id="037ea-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="037ea-106">Diese Methode verwendet angegebene Epsilon-Werte für Gleichheits Vergleiche.</span><span class="sxs-lookup"><span data-stu-id="037ea-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="037ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="037ea-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="037ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="037ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="037ea-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037ea-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="037ea-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="037ea-111">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) -Objekt, das Mesh, von dem Vertices geschweißt werden.</span><span class="sxs-lookup"><span data-stu-id="037ea-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="037ea-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="037ea-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="037ea-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="037ea-114">Eine Kombination aus einem oder mehreren Flags aus [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="037ea-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="037ea-115">*pepsilons* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037ea-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-116">Typ: **Konstanten [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="037ea-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="037ea-117">Zeiger auf eine [**D3DXWeldEpsilons**](d3dxweldepsilons.md) -Struktur, die die Epsilon-Werte angibt, die für diese Methode verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="037ea-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="037ea-118">Verwenden Sie **null** , um alle Strukturmember mit einem Standardwert von 1.0 e-6f zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="037ea-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="037ea-119">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="037ea-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-120">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="037ea-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="037ea-121">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt.</span><span class="sxs-lookup"><span data-stu-id="037ea-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="037ea-122">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="037ea-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="037ea-123">Wenn dieser Parameter auf **null** festgelegt ist, wird [**ID3DXBaseMesh:: generateseency**](id3dxbasemesh--generateadjacency.md) aufgerufen, um logische Informations Informationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="037ea-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="037ea-124">*padjacumcyout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="037ea-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="037ea-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="037ea-126">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="037ea-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="037ea-127">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="037ea-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="037ea-128">*pfakeremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="037ea-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-129">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="037ea-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="037ea-130">Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die jedem Gesicht im geschweißten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="037ea-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="037ea-131">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="037ea-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="037ea-132">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="037ea-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="037ea-133">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="037ea-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="037ea-134">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="037ea-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="037ea-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="037ea-135">Return value</span></span>

<span data-ttu-id="037ea-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="037ea-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="037ea-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="037ea-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="037ea-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="037ea-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="037ea-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="037ea-139">Remarks</span></span>

<span data-ttu-id="037ea-140">Diese Funktion verwendet die angegebenen Informationen zum Ermitteln der Punkte, die repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="037ea-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="037ea-141">Vertices werden auf Grundlage eines Epsilon-Vergleichs zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="037ea-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="037ea-142">Vertices mit gleicher Position müssen bereits berechnet und durch Punkt repräsentative Daten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="037ea-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="037ea-143">Diese Funktion kombiniert logisch versießte Scheitel Punkte, die ähnliche Komponenten aufweisen, wie z. b. normale oder Texturkoordinaten innerhalb von pepsilons.</span><span class="sxs-lookup"><span data-stu-id="037ea-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="037ea-144">Im folgenden Beispielcode wird diese Funktion mit aktiviertem Schweißen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="037ea-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="037ea-145">Vertices werden mithilfe von Epsilon-Werten für den normalen Vektor und die Scheitelpunkt Position verglichen.</span><span class="sxs-lookup"><span data-stu-id="037ea-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="037ea-146">Ein Zeiger wird an ein Flächen *kartogramm (pfakeremap*) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="037ea-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="037ea-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037ea-147">Requirements</span></span>



| <span data-ttu-id="037ea-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037ea-148">Requirement</span></span> | <span data-ttu-id="037ea-149">Wert</span><span class="sxs-lookup"><span data-stu-id="037ea-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="037ea-150">Header</span><span class="sxs-lookup"><span data-stu-id="037ea-150">Header</span></span><br/>  | <dl> <span data-ttu-id="037ea-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="037ea-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="037ea-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="037ea-152">Library</span></span><br/> | <dl> <span data-ttu-id="037ea-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="037ea-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="037ea-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037ea-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037ea-155">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="037ea-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
