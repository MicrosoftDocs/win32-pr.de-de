---
description: Enthält eine Gruppe von als Peers bewerteten andexp-Arrays.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Ausdrucks Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346074"
---
# <a name="expression-structure"></a><span data-ttu-id="7f9c3-103">Ausdrucks Struktur</span><span class="sxs-lookup"><span data-stu-id="7f9c3-103">EXPRESSION structure</span></span>

<span data-ttu-id="7f9c3-104">Die **Ausdrucks** Struktur enthält eine Gruppe von **andexp** -Arrays, die als Peers in logischen Ausdrücken und Ausdrücken ausgewertet werden, die das Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7f9c3-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="7f9c3-105">(Andexp 1 && andexp 2 && andexp 3).</span><span class="sxs-lookup"><span data-stu-id="7f9c3-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9c3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f9c3-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="7f9c3-107">Member</span><span class="sxs-lookup"><span data-stu-id="7f9c3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f9c3-108">**nandexps**</span><span class="sxs-lookup"><span data-stu-id="7f9c3-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="7f9c3-109">Anzahl von **andexp** -Mustern.</span><span class="sxs-lookup"><span data-stu-id="7f9c3-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="7f9c3-110">**Andexp**</span><span class="sxs-lookup"><span data-stu-id="7f9c3-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="7f9c3-111">Array von **andexp** -Mustern.</span><span class="sxs-lookup"><span data-stu-id="7f9c3-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="7f9c3-112">Der Erfassungs Filter ordnet alle Zeilen dieses Arrays als logische and-Anweisungen an.</span><span class="sxs-lookup"><span data-stu-id="7f9c3-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="7f9c3-113">Beachten Sie, dass jede Ausdrucks Struktur maximal vier **andexp** -Muster enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="7f9c3-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f9c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f9c3-114">Remarks</span></span>

<span data-ttu-id="7f9c3-115">Weitere Informationen zum Implementieren dieser Struktur als Teil eines Erfassungs Filters finden Sie unter [Capture Filters (Erfassen von Filtern](capture-filters.md)).</span><span class="sxs-lookup"><span data-stu-id="7f9c3-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f9c3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f9c3-116">Requirements</span></span>



| <span data-ttu-id="7f9c3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f9c3-117">Requirement</span></span> | <span data-ttu-id="7f9c3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7f9c3-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9c3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f9c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9c3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f9c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f9c3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f9c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9c3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f9c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f9c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f9c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f9c3-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c3-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f9c3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f9c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9c3-126">Andexp</span><span class="sxs-lookup"><span data-stu-id="7f9c3-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="7f9c3-127">Capturefilter</span><span class="sxs-lookup"><span data-stu-id="7f9c3-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




