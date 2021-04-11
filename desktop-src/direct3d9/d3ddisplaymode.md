---
description: Beschreibt den Anzeigemodus.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: D3DDISPLAYMODE-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132309"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="c986a-103">D3DDISPLAYMODE-Struktur</span><span class="sxs-lookup"><span data-stu-id="c986a-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="c986a-104">Beschreibt den Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="c986a-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c986a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c986a-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="c986a-106">Member</span><span class="sxs-lookup"><span data-stu-id="c986a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c986a-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="c986a-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c986a-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c986a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c986a-109">Bildschirmbreite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c986a-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c986a-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="c986a-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c986a-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c986a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c986a-112">Bildschirmhöhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c986a-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c986a-113">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c986a-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="c986a-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c986a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c986a-115">Aktualisierungsrate.</span><span class="sxs-lookup"><span data-stu-id="c986a-115">Refresh rate.</span></span> <span data-ttu-id="c986a-116">Der Wert 0 gibt einen Adapter Standard an.</span><span class="sxs-lookup"><span data-stu-id="c986a-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="c986a-117">**Format**</span><span class="sxs-lookup"><span data-stu-id="c986a-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="c986a-118">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c986a-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c986a-119">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format des Anzeigemodus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c986a-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c986a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c986a-120">Requirements</span></span>



| <span data-ttu-id="c986a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c986a-121">Requirement</span></span> | <span data-ttu-id="c986a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c986a-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c986a-123">Header</span><span class="sxs-lookup"><span data-stu-id="c986a-123">Header</span></span><br/> | <dl> <span data-ttu-id="c986a-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c986a-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c986a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c986a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c986a-126">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c986a-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c986a-127">**Enumadaptermodes**</span><span class="sxs-lookup"><span data-stu-id="c986a-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="c986a-128">**Getadapterdisplaymode**</span><span class="sxs-lookup"><span data-stu-id="c986a-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="c986a-129">**Getdisplaymode**</span><span class="sxs-lookup"><span data-stu-id="c986a-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
