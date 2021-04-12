---
description: Die Struktur "andexp" enthält ein Array von Muster Übereinstimmungen, mit denen Frame-Daten ausgewertet werden.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Andexp-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346838"
---
# <a name="andexp-structure"></a><span data-ttu-id="135e4-103">Andexp-Struktur</span><span class="sxs-lookup"><span data-stu-id="135e4-103">ANDEXP structure</span></span>

<span data-ttu-id="135e4-104">Die Struktur " **andexp** " enthält ein Array von Muster Übereinstimmungen, mit denen Frame-Daten ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="135e4-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="135e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="135e4-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="135e4-106">Member</span><span class="sxs-lookup"><span data-stu-id="135e4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="135e4-107">**npatternmatches**</span><span class="sxs-lookup"><span data-stu-id="135e4-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="135e4-108">Anzahl der Muster Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="135e4-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="135e4-109">**Patternmatch**</span><span class="sxs-lookup"><span data-stu-id="135e4-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="135e4-110">Array von Muster Übereinstimmungs Elementen.</span><span class="sxs-lookup"><span data-stu-id="135e4-110">Array of pattern match elements.</span></span> <span data-ttu-id="135e4-111">Beachten Sie, dass jede **andexp** -Struktur bis zu vier Muster Übereinstimmungs Elemente enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="135e4-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="135e4-112">Weitere Informationen zu diesem Member finden Sie unter [Erfassungs Filter](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="135e4-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="135e4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="135e4-113">Remarks</span></span>

<span data-ttu-id="135e4-114">Die Muster im Muster Array " **patternmatch** \[ Max \_ Patterns" \] werden als Peers in logischen OR-Anweisungen im Format verknüpft.</span><span class="sxs-lookup"><span data-stu-id="135e4-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="135e4-115">(Muster 1 \| \| Muster 2 \| \| Muster 3).</span><span class="sxs-lookup"><span data-stu-id="135e4-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="135e4-116">Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="135e4-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="135e4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="135e4-117">Requirements</span></span>



| <span data-ttu-id="135e4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="135e4-118">Requirement</span></span> | <span data-ttu-id="135e4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="135e4-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="135e4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="135e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="135e4-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="135e4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="135e4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="135e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="135e4-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="135e4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="135e4-124">Header</span><span class="sxs-lookup"><span data-stu-id="135e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="135e4-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="135e4-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135e4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="135e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135e4-127">Patternmatch</span><span class="sxs-lookup"><span data-stu-id="135e4-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




