---
description: Optionen zum Schweißen von Vertices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: D3DXWELDEPSILONSFLAGS-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355037"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="e1530-103">D3DXWELDEPSILONSFLAGS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e1530-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="e1530-104">Optionen zum Schweißen von Vertices.</span><span class="sxs-lookup"><span data-stu-id="e1530-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1530-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1530-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="e1530-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e1530-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1530-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ weldall**</span><span class="sxs-lookup"><span data-stu-id="e1530-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="e1530-108">Alle Scheitel Punkte, die sich am selben Speicherort befinden, werden verbunden.</span><span class="sxs-lookup"><span data-stu-id="e1530-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="e1530-109">Durch die Verwendung dieses Flags wird ein Epsilon-Vergleich zwischen Scheitelpunkt Komponenten vermieden.</span><span class="sxs-lookup"><span data-stu-id="e1530-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="e1530-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ weldpartialmatches**</span><span class="sxs-lookup"><span data-stu-id="e1530-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="e1530-111">Wenn eine bestimmte Scheitelpunkt Komponente innerhalb von Epsilon liegt, ändern Sie teilweise übereinstimmende Scheitel Punkte, sodass beide Komponenten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="e1530-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="e1530-112">Wenn alle Komponenten gleich sind, entfernen Sie eine der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="e1530-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e1530-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ donotrevevertices**</span><span class="sxs-lookup"><span data-stu-id="e1530-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="e1530-114">Weist das Schweißen an, nur Änderungen an Scheitel Punkten zu ermöglichen und nicht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e1530-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="e1530-115">Dieses Flag ist nur gültig, wenn D3DXWELDEPSILONS \_ weldpartialmatches festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e1530-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="e1530-116">Es ist hilfreich, die Scheitel Punkte so zu ändern, dass Sie gleich sind, aber nicht, um Vertices zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e1530-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e1530-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ donotsplit**</span><span class="sxs-lookup"><span data-stu-id="e1530-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="e1530-118">Weist das Schweißen an, Vertices nicht zu teilen, die sich in separaten Attribut Gruppen befinden.</span><span class="sxs-lookup"><span data-stu-id="e1530-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="e1530-119">Wenn die [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) -Methode mit dem D3DXMESHOPT \_ attrsort-Flag aufgerufen wird, wird das D3DXMESHOPT \_ donotsplit-Flag ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1530-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="e1530-120">Durch Festlegen dieses Flags kann die Verarbeitung von Software Scheitel Punkten verlangsamt werden.</span><span class="sxs-lookup"><span data-stu-id="e1530-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1530-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1530-121">Requirements</span></span>



| <span data-ttu-id="e1530-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1530-122">Requirement</span></span> | <span data-ttu-id="e1530-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e1530-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1530-124">Header</span><span class="sxs-lookup"><span data-stu-id="e1530-124">Header</span></span><br/> | <dl> <span data-ttu-id="e1530-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1530-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1530-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1530-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1530-127">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="e1530-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="e1530-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="e1530-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 




