---
title: MPCALLBACK_DATA Struktur (mpclient. h)
description: An die Rückruffunktion über gegebene Daten.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCALLBACK_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103567"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="7fb65-105">Mpcallback- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="7fb65-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="7fb65-106">An die Rückruffunktion über gegebene Daten.</span><span class="sxs-lookup"><span data-stu-id="7fb65-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fb65-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="7fb65-108">Member</span><span class="sxs-lookup"><span data-stu-id="7fb65-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fb65-109">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="7fb65-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-110">Typ: **[ **mpnotify**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb65-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-111">Ändern Sie die Benachrichtigung in den Bericht.</span><span class="sxs-lookup"><span data-stu-id="7fb65-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7fb65-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7fb65-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-114">Fehlercode im Falle eines internen Fehlers.</span><span class="sxs-lookup"><span data-stu-id="7fb65-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-115">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="7fb65-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-116">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="7fb65-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-117">Aktueller Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="7fb65-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="7fb65-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-119">Typ: **[ **mpcallback- \_ Typ**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb65-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-120">Spezieller Rückruf Datentyp.</span><span class="sxs-lookup"><span data-stu-id="7fb65-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-121">**Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-122">Rückruf-Sonderdaten.</span><span class="sxs-lookup"><span data-stu-id="7fb65-122">Callback special data.</span></span> <span data-ttu-id="7fb65-123">Der Zeiger auf die entsprechende-Struktur hängt vom Wert des **Typs** ab.</span><span class="sxs-lookup"><span data-stu-id="7fb65-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="7fb65-124">**pstatus Data**</span><span class="sxs-lookup"><span data-stu-id="7fb65-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-125">Typ: **pmpstatus- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-126">Wenn Sie  ==  **mpcallback- \_ Status** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="7fb65-127">Siehe [**mpstatus- \_ Daten**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-128">**pscandata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-129">Typ: **pmpscan- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-130">Beim **Typ**  ==  **mpcallback \_ Scan**.</span><span class="sxs-lookup"><span data-stu-id="7fb65-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="7fb65-131">Siehe [**mpscan- \_ Daten**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-132">**pcleandata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-133">Typ: **pmpclean- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-134">Wenn **Sie**  ==  **mpcallback \_ Bereinigen**.</span><span class="sxs-lookup"><span data-stu-id="7fb65-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="7fb65-135">Siehe [**mpclean \_ Data**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-136">**pprecheckdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-137">Type: **pmpclean \_ Precheck- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-138">Beim **Typ**  ==  **mpcallback \_ Precheck**.</span><span class="sxs-lookup"><span data-stu-id="7fb65-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="7fb65-139">Siehe [**mpclean \_ Precheck \_ Data**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-140">**p-Data**</span><span class="sxs-lookup"><span data-stu-id="7fb65-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-141">Typ: **pmpthreat- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-142">Beim **Typ**  ==  **mpcallback \_ Threat**.</span><span class="sxs-lookup"><span data-stu-id="7fb65-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="7fb65-143">Siehe [**mpthreat- \_ Daten**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-144">**psigupdatedata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-145">Typ: **pmpsigupdate- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-146">Wenn Sie  ==  **mpcallback \_ sigupdate** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="7fb65-147">Siehe [**mpsigupdate- \_ Daten**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-148">**psampledata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-149">Type: **pmpsample \_ Data**</span><span class="sxs-lookup"><span data-stu-id="7fb65-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-150">Wenn Sie  ==  **mpcallback- \_ Beispiel** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="7fb65-151">Siehe [**mpsample \_ Data**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-152">**preserveddata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-153">Typ: **pmbeibehaltene \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-154">Wenn der **Typ**  ==  **mpcallback \_ reserviert** ist.</span><span class="sxs-lookup"><span data-stu-id="7fb65-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="7fb65-155">Siehe [**mbeibehaltene \_ Daten**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-156">**pconfigurationdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-157">Typ: **pmpconfiguration- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-158">Wenn Sie  ==  **mpcallback- \_ Konfigurations \_ Benachrichtigung** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="7fb65-159">Siehe [**mpconfiguration \_ Data**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-160">**pfastpathdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-161">Typ: **pmpfastpath- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-162">Wenn Sie  ==  **mpcallback \_ FastPath** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="7fb65-163">Siehe [**mpfastpath- \_ Daten**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-164">**pexpirationdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-165">Typ: **\_ pmpabgelaufdaten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-166">Wenn Sie  ==  **mpcallback- \_ Produkt \_ Ablauf** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="7fb65-167">Siehe [**mpablauf- \_ Daten**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-168">**pnisprivatedata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-169">Typ: **pmpnis \_ private \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-170">Wenn Sie  ==  **mpcallback \_ NIS \_ private** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="7fb65-171">Weitere Informationen finden Sie unter [**mpnis \_ private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-172">**phealthdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-173">Typ: **pmphealth- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-174">Beim **Typ**  ==  **mpcallback \_ Health**.</span><span class="sxs-lookup"><span data-stu-id="7fb65-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="7fb65-175">Siehe [**mphealth- \_ Daten**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-176">**"pdoflifedata"**</span><span class="sxs-lookup"><span data-stu-id="7fb65-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-177">Typ: **\_ pmpendomelife-Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-178">Wenn Sie  ==  **mpcallback \_ endoentlife** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="7fb65-179">Weitere Informationen finden Sie unter [**\_ mpendomelife-Daten**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fb65-180">**pmalwaretoastdata**</span><span class="sxs-lookup"><span data-stu-id="7fb65-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="7fb65-181">Typ: **pmpmalwarepopup- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="7fb65-182">Wenn Sie  ==  **mpcallback \_ malwaretoast** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fb65-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="7fb65-183">Siehe [**mpmalwarepopup- \_ Daten**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="7fb65-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fb65-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fb65-184">Requirements</span></span>



| <span data-ttu-id="7fb65-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fb65-185">Requirement</span></span> | <span data-ttu-id="7fb65-186">Wert</span><span class="sxs-lookup"><span data-stu-id="7fb65-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb65-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fb65-187">Minimum supported client</span></span><br/> | <span data-ttu-id="7fb65-188">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fb65-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7fb65-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fb65-189">Minimum supported server</span></span><br/> | <span data-ttu-id="7fb65-190">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fb65-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fb65-191">Header</span><span class="sxs-lookup"><span data-stu-id="7fb65-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fb65-192"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb65-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb65-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fb65-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb65-194">**mpcallback- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="7fb65-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="7fb65-195">**mpclean- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-196">**mpclean- \_ vorprüf \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-197">**mpconfiguration- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-198">**\_mpendomelife-Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-199">**mpablauf- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-200">**mpfastpath- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-201">**mphealth- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-202">**mpmalwarepopup- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-203">**Private mpnis- \_ \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-204">**Mpnotify**</span><span class="sxs-lookup"><span data-stu-id="7fb65-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="7fb65-205">**mbeibehaltene \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-206">**mpsample- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-207">**mpscan- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-208">**mpsigupdate- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-209">**mpstatus- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="7fb65-210">**mpthreat- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7fb65-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





