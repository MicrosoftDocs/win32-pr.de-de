---
title: ADSI Print Job-Status Konstanten (adssts. h)
description: Die folgenden Konstanten werden mit der iadsprintjoboperations. Status-Eigenschaft verwendet, um den Status eines Druckauftrags anzugeben.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956914"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="7aebb-103">Status Konstanten für den ADSI-Druckauftrag</span><span class="sxs-lookup"><span data-stu-id="7aebb-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="7aebb-104">Die folgenden Konstanten werden mit der [**iadsprintjoboperations. Status**](iadsprintjoboperations-property-methods.md) -Eigenschaft verwendet, um den Status eines Druckauftrags anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7aebb-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="7aebb-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**Werbe \_ Auftrag \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="7aebb-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7aebb-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-107">Der Druckauftrag wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="7aebb-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS- \_ Auftrags \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="7aebb-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="7aebb-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-110">Ein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7aebb-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**Löschen eines ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7aebb-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="7aebb-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-113">Der Druckauftrag wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7aebb-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_ \_ Spoolvorgang für Werbeaufträge**</span><span class="sxs-lookup"><span data-stu-id="7aebb-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="7aebb-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-116">Der Druckauftrag wird gespoolte.</span><span class="sxs-lookup"><span data-stu-id="7aebb-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**Drucken von Werbe Aufträgen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7aebb-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="7aebb-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-119">Der Druckauftrag wird gedruckt.</span><span class="sxs-lookup"><span data-stu-id="7aebb-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS- \_ Auftrag \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="7aebb-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="7aebb-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-122">Der Drucker ist offline.</span><span class="sxs-lookup"><span data-stu-id="7aebb-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_ \_ Taschenbuch der Werbe Einblendung**</span><span class="sxs-lookup"><span data-stu-id="7aebb-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="7aebb-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-125">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="7aebb-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**Werbe \_ Auftrag \_ gedruckt**</span><span class="sxs-lookup"><span data-stu-id="7aebb-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="7aebb-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-128">Der Druckauftrag wurde gedruckt.</span><span class="sxs-lookup"><span data-stu-id="7aebb-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7aebb-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS- \_ Auftrag \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="7aebb-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aebb-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="7aebb-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="7aebb-131">Der Druckauftrag wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7aebb-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7aebb-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aebb-132">Requirements</span></span>



| <span data-ttu-id="7aebb-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aebb-133">Requirement</span></span> | <span data-ttu-id="7aebb-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7aebb-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7aebb-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aebb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7aebb-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7aebb-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="7aebb-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aebb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7aebb-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aebb-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="7aebb-139">Header</span><span class="sxs-lookup"><span data-stu-id="7aebb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aebb-140"><dt>Adssts. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aebb-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





