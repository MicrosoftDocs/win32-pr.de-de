---
description: Die Auftrags \_ Info \_ 3-Struktur wird verwendet, um einen Satz von Druckaufträgen miteinander zu verknüpfen.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: JOB_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218218"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="fed95-103">Auftrags \_ Info \_ 3-Struktur</span><span class="sxs-lookup"><span data-stu-id="fed95-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="fed95-104">Die **Auftrags \_ Info \_ 3** -Struktur wird verwendet, um einen Satz von Druckaufträgen miteinander zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="fed95-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed95-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fed95-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="fed95-106">Member</span><span class="sxs-lookup"><span data-stu-id="fed95-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fed95-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="fed95-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="fed95-108">Der Bezeichner des Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="fed95-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fed95-109">**Nextjobid**</span><span class="sxs-lookup"><span data-stu-id="fed95-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="fed95-110">Der Druckauftrags Bezeichner für den nächsten Druckauftrag in dem verknüpften Satz von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="fed95-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="fed95-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fed95-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fed95-112">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="fed95-112">This value is reserved for future use.</span></span> <span data-ttu-id="fed95-113">Sie müssen ihn auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="fed95-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fed95-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fed95-114">Requirements</span></span>



| <span data-ttu-id="fed95-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fed95-115">Requirement</span></span> | <span data-ttu-id="fed95-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fed95-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed95-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fed95-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fed95-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fed95-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fed95-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fed95-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fed95-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fed95-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fed95-121">Header</span><span class="sxs-lookup"><span data-stu-id="fed95-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed95-122"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fed95-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed95-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fed95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed95-124">Drucken</span><span class="sxs-lookup"><span data-stu-id="fed95-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fed95-125">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fed95-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fed95-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="fed95-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="fed95-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="fed95-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="fed95-128">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="fed95-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




