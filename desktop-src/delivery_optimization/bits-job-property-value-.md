---
title: BITS_JOB_PROPERTY_VALUE-Struktur (deliveryoptimization. h)
description: Die BITS_JOB_PROPERTY_VALUE Union stellt den Eigenschafts Wert des Do-Auftrags basierend auf dem Wert der BITS_JOB_PROPERTY_ID-Enumeration bereit.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE Struktur
- BITS_JOB_PROPERTY_VALUE Struktur
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103664"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="8b4c1-105">BITS_JOB_PROPERTY_VALUE Struktur</span><span class="sxs-lookup"><span data-stu-id="8b4c1-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="8b4c1-106">Die **BITS_JOB_PROPERTY_VALUE** Union stellt den Eigenschafts Wert des Do-Auftrags basierend auf dem Wert der [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) -Enumeration bereit.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b4c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b4c1-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="8b4c1-108">Member</span><span class="sxs-lookup"><span data-stu-id="8b4c1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b4c1-109">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-110">Dieser Wert wird zurückgegeben, wenn die Enumeration-Eigenschaften-ID verwendet wird **BITS_JOB_PROPERTY_ID_COST_FLAGS** und wird als [Übertragungs Richtlinie](https://www.bing.com/search?q=transfer+policy) für den Do-Auftrag angewendet.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="8b4c1-111">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-112">Dieser Wert wird zurückgegeben, wenn die enumerationseigenschafts-ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** verwendet wird, und stellt die CLSID des Rückruf Objekts dar, das bei der do-Aufgabe registriert werden soll</span><span class="sxs-lookup"><span data-stu-id="8b4c1-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="8b4c1-113">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-114">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8b4c1-115">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-116">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8b4c1-117">**Target**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-118">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b4c1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b4c1-119">Requirements</span></span>



| <span data-ttu-id="8b4c1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b4c1-120">Requirement</span></span> | <span data-ttu-id="8b4c1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8b4c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4c1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b4c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4c1-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b4c1-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b4c1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b4c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4c1-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b4c1-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b4c1-126">Header</span><span class="sxs-lookup"><span data-stu-id="8b4c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b4c1-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4c1-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4c1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b4c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4c1-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="8b4c1-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="8b4c1-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





