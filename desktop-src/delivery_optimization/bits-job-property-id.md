---
title: BITS_JOB_PROPERTY_ID-Enumeration (deliveryoptimization. h)
description: Die BITS_JOB_PROPERTY_ID-Enumeration gibt die ID der Eigenschaft für den Do-Auftrag an. Diese Enumeration wird in der BITS_JOB_PROPERTY_VALUE Union verwendet, um den Typ des Werts zu bestimmen, der in der Union enthalten ist.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- BITS_JOB_PROPERTY_ID-Enumeration
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740320"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="88c2b-105">BITS_JOB_PROPERTY_ID-Enumeration</span><span class="sxs-lookup"><span data-stu-id="88c2b-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="88c2b-106">Die **BITS_JOB_PROPERTY_ID** -Enumeration gibt die ID der Eigenschaft für den Do-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="88c2b-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="88c2b-107">Diese Enumeration wird in der [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union verwendet, um den Typ des Werts zu bestimmen, der in der Union enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="88c2b-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88c2b-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="88c2b-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="88c2b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88c2b-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="88c2b-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-111">Die ID, die verwendet wird, um das [Übertragungsverhalten](https://www.bing.com/search?q=control+transfer+behavior) über Mobilfunk-und/oder ähnliche Netzwerke zu steuern.</span><span class="sxs-lookup"><span data-stu-id="88c2b-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="88c2b-112">Diese Eigenschaft kann während einer laufenden Übertragung geändert werden. die neuen kostenflags werden sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="88c2b-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="88c2b-113">Diese Eigenschaft verwendet das **DWORD** -Feld **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="88c2b-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="88c2b-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-115">Die ID, die zum [Registrieren eines com-Rückrufs](https://www.bing.com/search?q=register+a+COM+callback) durch die CLSID verwendet wird, um Benachrichtigungen über den Fortschritt und den Abschluss eines do-Auftrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88c2b-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="88c2b-116">Die CLSID muss auf eine Klasse verweisen, die einem registrierten Prozess externen COM-Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="88c2b-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="88c2b-117">Sie kann auch auf **GUID_NULL** festgelegt werden, um eine zuvor festgelegte Benachrichtigungs-CLSID zu löschen.</span><span class="sxs-lookup"><span data-stu-id="88c2b-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="88c2b-118">Diese Eigenschaft verwendet das **CLSID** -Feld **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="88c2b-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="88c2b-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-120">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="88c2b-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-122">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="88c2b-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-124">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="88c2b-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-126">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="88c2b-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-128">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="88c2b-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="88c2b-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="88c2b-130">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c2b-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88c2b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88c2b-131">Requirements</span></span>



| <span data-ttu-id="88c2b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88c2b-132">Requirement</span></span> | <span data-ttu-id="88c2b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="88c2b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c2b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88c2b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="88c2b-135">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88c2b-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="88c2b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88c2b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="88c2b-137">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88c2b-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="88c2b-138">Header</span><span class="sxs-lookup"><span data-stu-id="88c2b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c2b-139"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c2b-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c2b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88c2b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c2b-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="88c2b-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="88c2b-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="88c2b-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="88c2b-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="88c2b-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="88c2b-144">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="88c2b-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="88c2b-145">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="88c2b-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





