---
description: Gibt das Quell Symbol und den Speicherort in einer Monochrom-Oberfläche an, in die Symbole kopiert werden sollen.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: D3DCOMPOSERECTDESTINATION-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355167"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="010d9-103">D3DCOMPOSERECTDESTINATION-Struktur</span><span class="sxs-lookup"><span data-stu-id="010d9-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="010d9-104">Gibt das Quell Symbol und den Speicherort in einer Monochrom-Oberfläche an, in die Symbole kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="010d9-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="010d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="010d9-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="010d9-106">Member</span><span class="sxs-lookup"><span data-stu-id="010d9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="010d9-107">**Srcrectindex**</span><span class="sxs-lookup"><span data-stu-id="010d9-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="010d9-108">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="010d9-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="010d9-109">Index bestimmtes Symbol aus dem Scheitelpunkt Puffer, der [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="010d9-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="010d9-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="010d9-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="010d9-111">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="010d9-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="010d9-112">Reserviert zu Ausrichtungs Zwecken.</span><span class="sxs-lookup"><span data-stu-id="010d9-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="010d9-113">**X**</span><span class="sxs-lookup"><span data-stu-id="010d9-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="010d9-114">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="010d9-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="010d9-115">Linke Koordinate, um mit dem Kopieren bei zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="010d9-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="010d9-116">**J**</span><span class="sxs-lookup"><span data-stu-id="010d9-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="010d9-117">Typ: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="010d9-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="010d9-118">Die obere Koordinate, an der der Kopiervorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="010d9-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="010d9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="010d9-119">Remarks</span></span>

<span data-ttu-id="010d9-120">Diese Struktur wird in Aufrufen von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um anzugeben, dass die Speicherort Symbole kopiert werden sollen und welches bestimmte Symbol kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="010d9-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="010d9-121">Ein Vertex-Puffer (siehe [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), der mit diesen Strukturen gefüllt ist, wird erstellt, um die Symbol Speicherorte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="010d9-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="010d9-122">Ushort-Mitglieder werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="010d9-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="010d9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="010d9-123">Requirements</span></span>



| <span data-ttu-id="010d9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="010d9-124">Requirement</span></span> | <span data-ttu-id="010d9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="010d9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="010d9-126">Header</span><span class="sxs-lookup"><span data-stu-id="010d9-126">Header</span></span><br/> | <dl> <span data-ttu-id="010d9-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="010d9-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010d9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="010d9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010d9-129">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="010d9-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
