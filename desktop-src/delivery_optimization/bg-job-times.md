---
title: BG_JOB_TIMES-Struktur (deliveryoptimization. h)
description: Die BG_JOB_TIMES-Struktur stellt auftragsbezogene Zeitstempel bereit.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- BG_JOB_TIMES Struktur
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740321"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="046a5-104">BG_JOB_TIMES Struktur</span><span class="sxs-lookup"><span data-stu-id="046a5-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="046a5-105">Die **BG_JOB_TIMES** -Struktur stellt auftragsbezogene Zeitstempel bereit.</span><span class="sxs-lookup"><span data-stu-id="046a5-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="046a5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="046a5-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="046a5-107">Member</span><span class="sxs-lookup"><span data-stu-id="046a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="046a5-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="046a5-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="046a5-109">Zeitpunkt, zu dem der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="046a5-109">Time the job was created.</span></span> <span data-ttu-id="046a5-110">Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.</span><span class="sxs-lookup"><span data-stu-id="046a5-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="046a5-111">**ModificationTime**</span><span class="sxs-lookup"><span data-stu-id="046a5-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="046a5-112">Uhrzeit, zu der der Auftrag zuletzt geändert wurde oder die Bytes übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="046a5-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="046a5-113">Durch das Hinzufügen von Dateien oder das Aufrufen einer der Set-Methoden in den [ \* *ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) -Schnittstellen wird dieser Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="046a5-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="046a5-114">Außerdem wird dieser Wert durch Änderungen am Status des Auftrags und durch Aufrufen der Methoden [_ *Suspend* \*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)und [**Complete**](ibackgroundcopyjob-complete.md) geändert.</span><span class="sxs-lookup"><span data-stu-id="046a5-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="046a5-115">Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.</span><span class="sxs-lookup"><span data-stu-id="046a5-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="046a5-116">**Transfercompletiontime**</span><span class="sxs-lookup"><span data-stu-id="046a5-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="046a5-117">Zeitpunkt, zu dem der Auftrag in den BG_JOB_STATE_TRANSFERRED Status eingetreten ist</span><span class="sxs-lookup"><span data-stu-id="046a5-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="046a5-118">Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.</span><span class="sxs-lookup"><span data-stu-id="046a5-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="046a5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="046a5-119">Requirements</span></span>



| <span data-ttu-id="046a5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="046a5-120">Requirement</span></span> | <span data-ttu-id="046a5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="046a5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="046a5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="046a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="046a5-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="046a5-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="046a5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="046a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="046a5-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="046a5-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="046a5-126">Header</span><span class="sxs-lookup"><span data-stu-id="046a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="046a5-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="046a5-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="046a5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="046a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046a5-129">**Ibackgroundcopyjob:: gettimes**</span><span class="sxs-lookup"><span data-stu-id="046a5-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

