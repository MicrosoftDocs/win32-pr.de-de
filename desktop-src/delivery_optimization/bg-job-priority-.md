---
title: BG_JOB_PRIORITY-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_PRIORITY-Enumeration definiert die Konstanten Werte, die die Prioritätsstufe eines Auftrags angeben.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY-Enumeration
- BG_JOB_PRIORITY-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040473"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="30a1b-105">BG_JOB_PRIORITY-Enumeration</span><span class="sxs-lookup"><span data-stu-id="30a1b-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="30a1b-106">Die **BG_JOB_PRIORITY** -Enumeration definiert die Konstanten Werte, die die Prioritätsstufe eines Auftrags angeben.</span><span class="sxs-lookup"><span data-stu-id="30a1b-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a1b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a1b-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="30a1b-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="30a1b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30a1b-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="30a1b-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="30a1b-110">Überträgt den Auftrag im Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="30a1b-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="30a1b-111">Vordergrund Übertragungen konkurrieren an der Netzwerkbandbreite mit anderen Anwendungen, die die Netzwerkleistung des Benutzers beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="30a1b-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="30a1b-112">Dies ist die höchste Prioritätsstufe.</span><span class="sxs-lookup"><span data-stu-id="30a1b-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="30a1b-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="30a1b-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="30a1b-114">Überträgt den Auftrag im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="30a1b-114">Transfers the job in the background.</span></span> <span data-ttu-id="30a1b-115">Bei Hintergrund Übertragungen wird ein kleiner Prozentsatz der Netzwerkbandbreite verwendet.</span><span class="sxs-lookup"><span data-stu-id="30a1b-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="30a1b-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="30a1b-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="30a1b-117">Do-Verhalten ist für alle nicht-Vordergrund-Aufträge identisch.</span><span class="sxs-lookup"><span data-stu-id="30a1b-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="30a1b-118">Ausführliche Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="30a1b-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="30a1b-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="30a1b-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="30a1b-120">Do-Verhalten ist für alle nicht-Vordergrund-Aufträge identisch.</span><span class="sxs-lookup"><span data-stu-id="30a1b-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="30a1b-121">Ausführliche Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="30a1b-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30a1b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30a1b-122">Remarks</span></span>

<span data-ttu-id="30a1b-123">Mehrere Vordergrund-und Hintergrund Übertragungen können gleichzeitig stattfinden.</span><span class="sxs-lookup"><span data-stu-id="30a1b-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a1b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a1b-124">Requirements</span></span>



| <span data-ttu-id="30a1b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30a1b-125">Requirement</span></span> | <span data-ttu-id="30a1b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="30a1b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a1b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30a1b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30a1b-128">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a1b-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="30a1b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30a1b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30a1b-130">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a1b-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="30a1b-131">Header</span><span class="sxs-lookup"><span data-stu-id="30a1b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a1b-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a1b-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a1b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a1b-134">**Ibackgroundcopyjob:: GetPriority**</span><span class="sxs-lookup"><span data-stu-id="30a1b-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="30a1b-135">**Ibackgroundcopyjob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="30a1b-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





