---
title: BG_JOB_TYPE-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_TYPE-Enumeration definiert konstante Werte, die den Typ des Übertragungs Auftrags angeben, z. b. den Download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- BG_JOB_TYPE-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476173"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="c464c-104">BG_JOB_TYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c464c-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="c464c-105">Die **BG_JOB_TYPE** -Enumeration definiert konstante Werte, die den Typ des Übertragungs Auftrags angeben, z. b. den Download.</span><span class="sxs-lookup"><span data-stu-id="c464c-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="c464c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c464c-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c464c-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c464c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c464c-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="c464c-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="c464c-109">Gibt an, dass der Auftrag Dateien auf den Client herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="c464c-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c464c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c464c-110">Requirements</span></span>



| <span data-ttu-id="c464c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c464c-111">Requirement</span></span> | <span data-ttu-id="c464c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c464c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c464c-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c464c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c464c-114">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c464c-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c464c-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c464c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c464c-116">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c464c-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c464c-117">Header</span><span class="sxs-lookup"><span data-stu-id="c464c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c464c-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c464c-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c464c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c464c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c464c-120">**Ibackgroundcopyjob:: GetType**</span><span class="sxs-lookup"><span data-stu-id="c464c-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="c464c-121">**Ibackgroundcopymanager:: kreatejob**</span><span class="sxs-lookup"><span data-stu-id="c464c-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





