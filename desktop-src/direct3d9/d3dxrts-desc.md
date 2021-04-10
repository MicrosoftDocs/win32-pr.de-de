---
description: Beschreibt eine Renderoberfläche.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC-Struktur (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961593"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="ca909-103">D3DXRTS- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="ca909-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="ca909-104">Beschreibt eine Renderoberfläche.</span><span class="sxs-lookup"><span data-stu-id="ca909-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca909-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca909-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="ca909-106">Member</span><span class="sxs-lookup"><span data-stu-id="ca909-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca909-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="ca909-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ca909-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca909-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca909-109">Breite der Renderoberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ca909-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ca909-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="ca909-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ca909-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca909-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca909-112">Höhe der Renderoberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ca909-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ca909-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="ca909-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ca909-114">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ca909-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca909-115">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Renderoberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca909-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="ca909-116">**Depthstencil**</span><span class="sxs-lookup"><span data-stu-id="ca909-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="ca909-117">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca909-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca909-118">**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt. Andernfalls ist dieser Member auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca909-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ca909-119">**Depthstencilformat**</span><span class="sxs-lookup"><span data-stu-id="ca909-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ca909-120">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ca909-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca909-121">Wenn depthstencil auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Renderoberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca909-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca909-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca909-122">Requirements</span></span>



| <span data-ttu-id="ca909-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca909-123">Requirement</span></span> | <span data-ttu-id="ca909-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ca909-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca909-125">Header</span><span class="sxs-lookup"><span data-stu-id="ca909-125">Header</span></span><br/> | <dl> <span data-ttu-id="ca909-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca909-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca909-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca909-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca909-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ca909-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="ca909-129">**ID3DXRenderToSurface:: getdebug**</span><span class="sxs-lookup"><span data-stu-id="ca909-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
