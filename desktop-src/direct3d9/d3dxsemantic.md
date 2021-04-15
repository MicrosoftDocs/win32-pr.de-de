---
description: Semantik ordnet einem Scheitelpunkt-oder Pixel-Shader-Register einen Parameter zu. Sie können auch optionale beschreibende Zeichen folgen sein, die an nicht-Register Parameter angefügt sind.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: D3DXSEMANTIC-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394105"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="a1d3b-104">D3DXSEMANTIC-Struktur</span><span class="sxs-lookup"><span data-stu-id="a1d3b-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="a1d3b-105">Semantik ordnet einem Scheitelpunkt-oder Pixel-Shader-Register einen Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="a1d3b-106">Sie können auch optionale beschreibende Zeichen folgen sein, die an nicht-Register Parameter angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1d3b-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="a1d3b-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1d3b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1d3b-109">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="a1d3b-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="a1d3b-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d3b-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1d3b-111">Optionen, die bestimmen, wie Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-111">Options that identify how resources are used.</span></span> <span data-ttu-id="a1d3b-112">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="a1d3b-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d3b-113">**Start Index**</span><span class="sxs-lookup"><span data-stu-id="a1d3b-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a1d3b-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d3b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1d3b-115">Optionen, die die Interpretation der Verwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="a1d3b-116">Der Verwendungs-und Verwendungs Index bilden eine Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="a1d3b-117">Siehe [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="a1d3b-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1d3b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1d3b-118">Remarks</span></span>

<span data-ttu-id="a1d3b-119">Die Semantik ist für Scheitelpunkt-und Pixel-Shader, Eingabe-und Ausgabe Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1d3b-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d3b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1d3b-120">Requirements</span></span>



| <span data-ttu-id="a1d3b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1d3b-121">Requirement</span></span> | <span data-ttu-id="a1d3b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a1d3b-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d3b-123">Header</span><span class="sxs-lookup"><span data-stu-id="a1d3b-123">Header</span></span><br/> | <dl> <span data-ttu-id="a1d3b-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1d3b-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d3b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1d3b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d3b-126">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="a1d3b-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
