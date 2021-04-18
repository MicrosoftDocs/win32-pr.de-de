---
description: Generiert ein vereinfachtes Mesh mit den bereitgestellten Gewichtungen, die so nah wie möglich für den angegebenen MinValue sind.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: D3DXSimplifyMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355006"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="6129e-103">D3DXSimplifyMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="6129e-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="6129e-104">Generiert ein vereinfachtes Mesh mit den bereitgestellten Gewichtungen, die so nah wie möglich für den angegebenen MinValue sind.</span><span class="sxs-lookup"><span data-stu-id="6129e-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="6129e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6129e-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="6129e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6129e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6129e-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6129e-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6129e-109">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das quellmesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="6129e-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-110">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-111">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6129e-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6129e-112">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, das vereinfacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="6129e-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-113">*pvertexattributegewichtungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-114">Typ: **Konstanten [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="6129e-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="6129e-115">Zeiger auf eine [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) -Struktur, die die Gewichtung für jede Scheitelpunkt Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="6129e-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="6129e-116">Wenn dieser Parameter auf **null** festgelegt ist, wird eine Standardstruktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="6129e-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="6129e-117">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6129e-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-118">*pvertexgewichtungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-119">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6129e-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6129e-120">Zeiger auf ein Array von Vertex-Gewichtungen.</span><span class="sxs-lookup"><span data-stu-id="6129e-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="6129e-121">Wenn dieser Parameter auf **null** festgelegt ist, werden alle Scheitelpunkt Gewichtungen auf 1,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6129e-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-122">*MinValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6129e-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6129e-124">Anzahl der Scheitel Punkte oder Gesichter, abhängig von dem im *options* -Parameter festgelegten Flag, um das quellmesh zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="6129e-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-125">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6129e-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6129e-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6129e-127">Gibt Vereinfachungs Optionen für das Mesh an.</span><span class="sxs-lookup"><span data-stu-id="6129e-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="6129e-128">Eines der Flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) kann festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6129e-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="6129e-129">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6129e-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6129e-130">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6129e-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6129e-131">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zurückgegebene Vereinfachungs Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="6129e-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6129e-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6129e-132">Return value</span></span>

<span data-ttu-id="6129e-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6129e-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6129e-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6129e-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6129e-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="6129e-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6129e-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6129e-136">Remarks</span></span>

<span data-ttu-id="6129e-137">Diese Funktion generiert ein Mesh, das über *MinValue* -Scheitel Punkte oder Gesichter verfügt.</span><span class="sxs-lookup"><span data-stu-id="6129e-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="6129e-138">Wenn das Mesh durch den Vereinfachungsprozess nicht auf *MinValue* reduziert werden kann, ist der-Vorgang weiterhin erfolgreich, da *MinValue* ein gewünschter Minimalwert und kein absolutes Minimalwert ist.</span><span class="sxs-lookup"><span data-stu-id="6129e-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="6129e-139">Wenn *pvertexattributegewichtungen* auf **null** festgelegt ist, werden die folgenden Werte der [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) -Standardstruktur zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6129e-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="6129e-140">Diese Standardstruktur sollte von den meisten Anwendungen verwendet werden, da Sie nur eine geometrische und normale Anpassung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6129e-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="6129e-141">Nur in besonderen Fällen müssen die anderen Mitglieds Felder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6129e-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="6129e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6129e-142">Requirements</span></span>



| <span data-ttu-id="6129e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6129e-143">Requirement</span></span> | <span data-ttu-id="6129e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="6129e-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6129e-145">Header</span><span class="sxs-lookup"><span data-stu-id="6129e-145">Header</span></span><br/>  | <dl> <span data-ttu-id="6129e-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6129e-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6129e-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6129e-147">Library</span></span><br/> | <dl> <span data-ttu-id="6129e-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6129e-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6129e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6129e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6129e-150">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6129e-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
