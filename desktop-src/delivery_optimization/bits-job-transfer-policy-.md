---
title: BITS_JOB_TRANSFER_POLICY-Enumeration (deliveryoptimization. h)
description: Die BITS_JOB_TRANSFER_POLICY-Enumeration definiert ID-Werte, die den Do-Eigenschaften entsprechen.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- BITS_JOB_TRANSFER_POLICY-Enumeration
- BITS_JOB_TRANSFER_POLICY-Enumeration
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103243"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="9ca69-105">BITS_JOB_TRANSFER_POLICY-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9ca69-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="9ca69-106">Die **BITS_JOB_TRANSFER_POLICY** -Enumeration definiert ID-Werte, die den Do-Eigenschaften entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9ca69-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca69-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ca69-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="9ca69-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9ca69-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9ca69-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="9ca69-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="9ca69-110">Gibt an, dass der Auftrag übertragen wird, wenn die Konnektivität unabhängig von den Kosten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9ca69-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="9ca69-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="9ca69-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="9ca69-112">Gibt an, dass der Auftrag übertragen wird, wenn eine Verbindung verfügbar ist, es sei denn, die Konnektivität unterliegt roamingzuschläge.</span><span class="sxs-lookup"><span data-stu-id="9ca69-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="9ca69-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="9ca69-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="9ca69-114">Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die keinem Zuschlag unterliegt.</span><span class="sxs-lookup"><span data-stu-id="9ca69-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="9ca69-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="9ca69-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="9ca69-116">Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die weder einem Aufpreis noch der beinahe-Erschöpfung unterliegt.</span><span class="sxs-lookup"><span data-stu-id="9ca69-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="9ca69-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="9ca69-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="9ca69-118">Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die keine Kosten oder Datenverkehrs Limits vorsieht.</span><span class="sxs-lookup"><span data-stu-id="9ca69-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ca69-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ca69-119">Requirements</span></span>



| <span data-ttu-id="9ca69-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ca69-120">Requirement</span></span> | <span data-ttu-id="9ca69-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9ca69-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca69-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ca69-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca69-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ca69-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9ca69-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ca69-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca69-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ca69-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ca69-126">Header</span><span class="sxs-lookup"><span data-stu-id="9ca69-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ca69-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca69-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





