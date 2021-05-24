---
description: Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Gitters.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D rawSubsetInstanced-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335634"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="6df14-103">ID3DX10Mesh::D rawSubsetInstanced-Methode</span><span class="sxs-lookup"><span data-stu-id="6df14-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="6df14-104">Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Gitters.</span><span class="sxs-lookup"><span data-stu-id="6df14-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6df14-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="6df14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6df14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df14-107">*AttribId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6df14-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df14-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6df14-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6df14-109">Gibt an, welche Teilmenge des Gitters ge zeichnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6df14-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="6df14-110">Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als einer oder mehrere Attributgruppen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6df14-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="6df14-111">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="6df14-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6df14-112">*InstanceCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6df14-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df14-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6df14-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6df14-114">Anzahl der zu rendernden Instanzen.</span><span class="sxs-lookup"><span data-stu-id="6df14-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="6df14-115">*StartInstanceLocation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6df14-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df14-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6df14-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6df14-117">Die Instanz, aus der in jedem Puffer, der als Instanzdaten markiert ist, abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6df14-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df14-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6df14-118">Return value</span></span>

<span data-ttu-id="6df14-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6df14-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6df14-120">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="6df14-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6df14-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6df14-121">Remarks</span></span>

<span data-ttu-id="6df14-122">Ein Gitternetz enthält eine Attributtabelle.</span><span class="sxs-lookup"><span data-stu-id="6df14-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="6df14-123">Die Attributtabelle kann ein Gitternetz in Teilmengen unterteilen, wobei jede Teilmenge mit einer Attribut-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6df14-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="6df14-124">Ein Gitternetz mit 200 Gesichtern, unterteilt in drei Teilmengen, kann beispielsweise eine Attributtabelle wie die folgende haben:</span><span class="sxs-lookup"><span data-stu-id="6df14-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="6df14-125">Subset</span><span class="sxs-lookup"><span data-stu-id="6df14-125">Subset</span></span>     | <span data-ttu-id="6df14-126">Gesichtserkennung</span><span class="sxs-lookup"><span data-stu-id="6df14-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="6df14-127">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="6df14-127">AttribID 0</span></span> | <span data-ttu-id="6df14-128">Gesichter 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="6df14-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="6df14-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="6df14-129">AttribID 1</span></span> | <span data-ttu-id="6df14-130">Gesichter 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="6df14-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="6df14-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="6df14-131">AttribID 2</span></span> | <span data-ttu-id="6df14-132">Gesichter 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="6df14-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="6df14-133">Die Instanziierung kann die Leistung erweitern, indem dieselbe Geometrie wiederverwendet wird, um mehrere Objekte in einer Szene zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6df14-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="6df14-134">Ein Beispiel für die Instanziierung ist das Zeichnen desselben Objekts mit unterschiedlichen Positionen und Farben.</span><span class="sxs-lookup"><span data-stu-id="6df14-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="6df14-135">Die Indizierung erfordert mehrere Scheitelpunktpuffer: mindestens einen für Daten pro Scheitelpunkt und einen zweiten Puffer für Daten pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="6df14-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="6df14-136">Zeichnungsinstanzen mit DrawSubsetInstanced ähneln sehr dem Prozess, der mit [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) verwendet wird, der im [Instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="6df14-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="6df14-137">Der Hauptunterschied bei der Verwendung von DrawSubsetInstanced besteht darin, dass Scheitelpunkt- und Indexpuffer aus dem [**ID3DX10Mesh-Schnittstellenobjekt**](id3dx10mesh.md) extrahiert werden müssen, bevor die Instanziierungsdaten kombiniert werden können.</span><span class="sxs-lookup"><span data-stu-id="6df14-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="6df14-138">Der folgende Code veranschaulicht das Extrahieren der Scheitelpunkt- und Indexpuffer aus dem Gittermodellobjekt.</span><span class="sxs-lookup"><span data-stu-id="6df14-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="6df14-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6df14-139">Requirements</span></span>



| <span data-ttu-id="6df14-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6df14-140">Requirement</span></span> | <span data-ttu-id="6df14-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6df14-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6df14-142">Header</span><span class="sxs-lookup"><span data-stu-id="6df14-142">Header</span></span><br/>  | <dl> <span data-ttu-id="6df14-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="6df14-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6df14-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6df14-144">Library</span></span><br/> | <dl> <span data-ttu-id="6df14-145"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df14-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df14-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6df14-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df14-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="6df14-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="6df14-148">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6df14-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
