---
description: Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D rawsubsegtinstanzierte-Methode (d3dx10. h)
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
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353385"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="5cf7d-103">ID3DX10Mesh::D rawsubsegtinstanzierte-Methode</span><span class="sxs-lookup"><span data-stu-id="5cf7d-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="5cf7d-104">Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Mesh.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cf7d-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="5cf7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cf7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf7d-107">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cf7d-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cf7d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cf7d-109">Gibt an, welche Teilmenge des Mesh gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="5cf7d-110">Dieser Wert wird verwendet, um Gesichter in einem Mesh als zu einer oder mehreren Attribut Gruppen gehörenden zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="5cf7d-111">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5cf7d-112">*InstanceCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cf7d-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cf7d-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cf7d-114">Anzahl der zu Rendering enden Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="5cf7d-115">*Startinstancelokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cf7d-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cf7d-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cf7d-117">Die Instanz, aus der in jedem als Instanzdaten markierten Puffer abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf7d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cf7d-118">Return value</span></span>

<span data-ttu-id="5cf7d-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5cf7d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5cf7d-120">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf7d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cf7d-121">Remarks</span></span>

<span data-ttu-id="5cf7d-122">Ein Mesh enthält eine Attribut Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="5cf7d-123">In der Attribut Tabelle kann ein Mesh in Teilmengen aufgeteilt werden, wobei jede Teilmenge mit einer Attribut-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="5cf7d-124">Beispielsweise kann ein Mesh mit 200-Gesichtern, das in drei Teilmengen unterteilt ist, eine Attribut Tabelle aufweisen, die wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="5cf7d-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



|            |                 |
|------------|-----------------|
| <span data-ttu-id="5cf7d-125">Atungbid 0</span><span class="sxs-lookup"><span data-stu-id="5cf7d-125">AttribID 0</span></span> | <span data-ttu-id="5cf7d-126">Gesichter 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="5cf7d-126">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="5cf7d-127">Atungbid 1</span><span class="sxs-lookup"><span data-stu-id="5cf7d-127">AttribID 1</span></span> | <span data-ttu-id="5cf7d-128">Gesichter 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="5cf7d-128">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="5cf7d-129">Atungbid 2</span><span class="sxs-lookup"><span data-stu-id="5cf7d-129">AttribID 2</span></span> | <span data-ttu-id="5cf7d-130">Gesichter 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="5cf7d-130">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="5cf7d-131">Durch die Instanziierung kann die Leistung durch Wiederverwendung derselben Geometrie erweitert werden, um mehrere Objekte in einer Szene zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-131">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="5cf7d-132">Ein Beispiel für eine Instanziierung könnte darin bestehen, das gleiche Objekt mit unterschiedlichen Positionen und Farben zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-132">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="5cf7d-133">Die Indizierung erfordert mehrere Vertex-Puffer: mindestens eine für pro-Vertex-Daten und einen zweiten Puffer für Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-133">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="5cf7d-134">Das Zeichnen von Instanzen mit drawsubmentinstancing ähnelt dem Prozess, der mit [**ID3D10Device verwendet wird::D rawindexedinstancing**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) , der unter [Instancing Sample (instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)) beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-134">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="5cf7d-135">Der Hauptunterschied bei der Verwendung von drawsubsetinstancing besteht darin, dass Vertex-und Index Puffer aus dem [**ID3DX10Mesh-Schnittstellen**](id3dx10mesh.md) Objekt extrahiert werden müssen, bevor die Instanziierungsdaten kombiniert werden können.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-135">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="5cf7d-136">Der folgende Code veranschaulicht das Extrahieren der Scheitelpunkt-und Index Puffer aus dem Mesh-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5cf7d-136">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="5cf7d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cf7d-137">Requirements</span></span>



| <span data-ttu-id="5cf7d-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cf7d-138">Requirement</span></span> | <span data-ttu-id="5cf7d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="5cf7d-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf7d-140">Header</span><span class="sxs-lookup"><span data-stu-id="5cf7d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="5cf7d-141"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cf7d-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5cf7d-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5cf7d-142">Library</span></span><br/> | <dl> <span data-ttu-id="5cf7d-143"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5cf7d-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf7d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cf7d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf7d-145">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5cf7d-145">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5cf7d-146">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5cf7d-146">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
