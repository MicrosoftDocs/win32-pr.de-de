---
description: Gibt die Typen der Anzeigemodi an, die herausgefiltert werden sollen.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: D3DDISPLAYMODEFILTER-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354466"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="b5b7d-103">D3DDISPLAYMODEFILTER-Struktur</span><span class="sxs-lookup"><span data-stu-id="b5b7d-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="b5b7d-104">Gibt die Typen der Anzeigemodi an, die herausgefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5b7d-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="b5b7d-106">Member</span><span class="sxs-lookup"><span data-stu-id="b5b7d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5b7d-107">**Größe**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b5b7d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5b7d-109">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-109">The size of this structure.</span></span> <span data-ttu-id="b5b7d-110">Diese sollte immer auf sizeof (D3DDISPLAYMODEFILTER) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="b5b7d-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b5b7d-112">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5b7d-113">Das auszufilternde Anzeigemodus-Format. Siehe [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="b5b7d-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5b7d-114">**Scanlineorder**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="b5b7d-115">Typ: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5b7d-116">Ob die Scanline-Reihenfolge Zeilen Sprung oder progressiv ist.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="b5b7d-117">Siehe [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="b5b7d-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5b7d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5b7d-118">Requirements</span></span>



| <span data-ttu-id="b5b7d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5b7d-119">Requirement</span></span> | <span data-ttu-id="b5b7d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5b7d-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b7d-121">Header</span><span class="sxs-lookup"><span data-stu-id="b5b7d-121">Header</span></span><br/> | <dl> <span data-ttu-id="b5b7d-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b7d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5b7d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b7d-124">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b5b7d-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
