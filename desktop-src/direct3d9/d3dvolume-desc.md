---
description: Beschreibt ein Volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: D3DVOLUME_DESC-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355187"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="bab6c-103">D3DVOLUME- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="bab6c-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="bab6c-104">Beschreibt ein Volume.</span><span class="sxs-lookup"><span data-stu-id="bab6c-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab6c-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="bab6c-106">Member</span><span class="sxs-lookup"><span data-stu-id="bab6c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bab6c-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="bab6c-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-108">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-109">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format des Volumes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bab6c-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="bab6c-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-111">Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-112">Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Volume identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bab6c-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-113">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="bab6c-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-115">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bab6c-115">Currently not used.</span></span> <span data-ttu-id="bab6c-116">Wird immer als 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bab6c-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="bab6c-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-118">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-119">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für dieses Volume zugewiesene Arbeitsspeicher Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="bab6c-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-120">**Width**</span><span class="sxs-lookup"><span data-stu-id="bab6c-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-122">Breite des Volumes in Pixel.</span><span class="sxs-lookup"><span data-stu-id="bab6c-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-123">**Height**</span><span class="sxs-lookup"><span data-stu-id="bab6c-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-125">Höhe des Volumes in Pixel.</span><span class="sxs-lookup"><span data-stu-id="bab6c-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bab6c-126">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="bab6c-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="bab6c-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab6c-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab6c-128">Die Tiefe des Volumes in Pixel.</span><span class="sxs-lookup"><span data-stu-id="bab6c-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bab6c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bab6c-129">Requirements</span></span>



| <span data-ttu-id="bab6c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bab6c-130">Requirement</span></span> | <span data-ttu-id="bab6c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bab6c-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab6c-132">Header</span><span class="sxs-lookup"><span data-stu-id="bab6c-132">Header</span></span><br/> | <dl> <span data-ttu-id="bab6c-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab6c-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab6c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bab6c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab6c-135">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bab6c-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="bab6c-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="bab6c-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="bab6c-137">**Getleveldebug**</span><span class="sxs-lookup"><span data-stu-id="bab6c-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
