---
description: Statistiken zur Ressourcennutzung.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_RESOURCEMANAGER-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129979"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="82d48-103">D3DDEVINFO \_ RESOURCEMANAGER-Struktur</span><span class="sxs-lookup"><span data-stu-id="82d48-103">D3DDEVINFO\_RESOURCEMANAGER structure</span></span>

<span data-ttu-id="82d48-104">Statistiken zur Ressourcennutzung.</span><span class="sxs-lookup"><span data-stu-id="82d48-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82d48-105">Syntax</span></span>


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a><span data-ttu-id="82d48-106">Member</span><span class="sxs-lookup"><span data-stu-id="82d48-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82d48-107">**stats**</span><span class="sxs-lookup"><span data-stu-id="82d48-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="82d48-108">Typ: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="82d48-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82d48-109">Array von Ressourcenstatistikelementen.</span><span class="sxs-lookup"><span data-stu-id="82d48-109">Array of resource statistics elements.</span></span> <span data-ttu-id="82d48-110">Siehe [**D3DRESOURCESTATS.**](d3dresourcestats.md)</span><span class="sxs-lookup"><span data-stu-id="82d48-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d48-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82d48-111">Remarks</span></span>

<span data-ttu-id="82d48-112">D3DRTYPECOUNT bezieht sich auf die Anzahl der Enumerationen in [**D3DRESOURCETYPE.**](./d3dresourcetype.md)</span><span class="sxs-lookup"><span data-stu-id="82d48-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82d48-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82d48-113">Requirements</span></span>



| <span data-ttu-id="82d48-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82d48-114">Requirement</span></span> | <span data-ttu-id="82d48-115">Wert</span><span class="sxs-lookup"><span data-stu-id="82d48-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82d48-116">Header</span><span class="sxs-lookup"><span data-stu-id="82d48-116">Header</span></span><br/> | <dl> <span data-ttu-id="82d48-117"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="82d48-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d48-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82d48-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d48-119">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="82d48-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
