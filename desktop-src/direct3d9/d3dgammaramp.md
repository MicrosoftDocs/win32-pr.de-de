---
description: Enthält rote, grüne und blaue Daten.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: D3DGAMMARAMP-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370440"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="021ff-103">D3DGAMMARAMP-Struktur</span><span class="sxs-lookup"><span data-stu-id="021ff-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="021ff-104">Enthält rote, grüne und blaue Daten.</span><span class="sxs-lookup"><span data-stu-id="021ff-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="021ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="021ff-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="021ff-106">Member</span><span class="sxs-lookup"><span data-stu-id="021ff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="021ff-107">**Red**</span><span class="sxs-lookup"><span data-stu-id="021ff-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="021ff-108">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="021ff-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="021ff-109">Ein Array von 256 Word-Elementen, das die rote Gamma-Rampe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="021ff-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="021ff-110">**Grünbuchs**</span><span class="sxs-lookup"><span data-stu-id="021ff-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="021ff-111">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="021ff-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="021ff-112">Ein Array von 256 Word-Elementen, das die grüne Gamma-Rampe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="021ff-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="021ff-113">**blauen**</span><span class="sxs-lookup"><span data-stu-id="021ff-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="021ff-114">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="021ff-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="021ff-115">Ein Array von 256 Word-Elementen, das die blaue Gamma-Rampe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="021ff-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="021ff-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="021ff-116">Requirements</span></span>



| <span data-ttu-id="021ff-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="021ff-117">Requirement</span></span> | <span data-ttu-id="021ff-118">Wert</span><span class="sxs-lookup"><span data-stu-id="021ff-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="021ff-119">Header</span><span class="sxs-lookup"><span data-stu-id="021ff-119">Header</span></span><br/> | <dl> <span data-ttu-id="021ff-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="021ff-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021ff-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="021ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021ff-122">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="021ff-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="021ff-123">**Getgammaramp**</span><span class="sxs-lookup"><span data-stu-id="021ff-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="021ff-124">**Setgammaramp**</span><span class="sxs-lookup"><span data-stu-id="021ff-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
