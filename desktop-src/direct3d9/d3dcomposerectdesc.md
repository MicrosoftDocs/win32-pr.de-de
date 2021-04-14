---
description: Gibt das Rechteck an, das verwendet wird, um Symbole auf eine monochrome Oberfläche einzuschließen.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: D3DCOMPOSERECTDESC-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394078"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="d0538-103">D3DCOMPOSERECTDESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="d0538-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="d0538-104">Gibt das Rechteck an, das verwendet wird, um Symbole auf eine monochrome Oberfläche einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d0538-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0538-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0538-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="d0538-106">Member</span><span class="sxs-lookup"><span data-stu-id="d0538-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0538-107">**X**</span><span class="sxs-lookup"><span data-stu-id="d0538-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="d0538-108">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0538-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0538-109">Linke Koordinate, um mit dem Kopieren bei zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d0538-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="d0538-110">**J**</span><span class="sxs-lookup"><span data-stu-id="d0538-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="d0538-111">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0538-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0538-112">Die obere Koordinate, an der der Kopiervorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="d0538-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="d0538-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="d0538-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d0538-114">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0538-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0538-115">Anzahl von texeln von linker Koordinate.</span><span class="sxs-lookup"><span data-stu-id="d0538-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d0538-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="d0538-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d0538-117">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0538-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0538-118">Die Anzahl von texeln aus der oberen Koordinate.</span><span class="sxs-lookup"><span data-stu-id="d0538-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0538-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0538-119">Remarks</span></span>

<span data-ttu-id="d0538-120">Diese Struktur wird in Aufrufen von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um Symbole auf der Quell Oberfläche einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d0538-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="d0538-121">Ein Vertex-Puffer (siehe [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), der mit diesen Strukturen gefüllt ist, wird erstellt, um die Symbol Speicherorte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="d0538-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="d0538-122">Ushort-Mitglieder werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="d0538-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0538-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0538-123">Requirements</span></span>



| <span data-ttu-id="d0538-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0538-124">Requirement</span></span> | <span data-ttu-id="d0538-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d0538-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0538-126">Header</span><span class="sxs-lookup"><span data-stu-id="d0538-126">Header</span></span><br/> | <dl> <span data-ttu-id="d0538-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0538-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0538-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0538-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0538-129">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d0538-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
