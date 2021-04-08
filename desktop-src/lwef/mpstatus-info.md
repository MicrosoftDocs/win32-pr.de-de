---
title: MPSTATUS_INFO Struktur (mpclient. h)
description: Status Informationen für den Malware Schutz-Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSTATUS_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740129"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="5b430-105">Mpstatus- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="5b430-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="5b430-106">Status Informationen für den Malware Schutz-Manager.</span><span class="sxs-lookup"><span data-stu-id="5b430-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b430-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b430-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="5b430-108">Member</span><span class="sxs-lookup"><span data-stu-id="5b430-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b430-109">**Productstatus**</span><span class="sxs-lookup"><span data-stu-id="5b430-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5b430-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-111">Gesamtprodukt Status.</span><span class="sxs-lookup"><span data-stu-id="5b430-111">Overall product status.</span></span> <span data-ttu-id="5b430-112">Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="5b430-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b430-113">**Lastquickscan**</span><span class="sxs-lookup"><span data-stu-id="5b430-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-114">Typ: **[ **mpscan- \_ Ergebnis**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="5b430-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-115">Ergebnisse der letzten Überprüfung durch den Malware Schutz-Manager.</span><span class="sxs-lookup"><span data-stu-id="5b430-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="5b430-116">Siehe [**mpscan- \_ Ergebnis**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="5b430-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b430-117">**Lastfullscan**</span><span class="sxs-lookup"><span data-stu-id="5b430-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-118">Typ: **[ **mpscan- \_ Ergebnis**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="5b430-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-119">Ergebnisse der letzten vollständigen Überprüfung durch den Malware Schutz-Manager.</span><span class="sxs-lookup"><span data-stu-id="5b430-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="5b430-120">Siehe [**mpscan- \_ Ergebnis**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="5b430-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b430-121">**Bedrohlich stats**</span><span class="sxs-lookup"><span data-stu-id="5b430-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-122">Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="5b430-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-123">Aktive Bedrohungs Statistiken.</span><span class="sxs-lookup"><span data-stu-id="5b430-123">Active threat statistics.</span></span> <span data-ttu-id="5b430-124">Siehe [**mpthreat \_ Stats**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="5b430-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b430-125">**Status**</span><span class="sxs-lookup"><span data-stu-id="5b430-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-126">Typ: **[**mpthreat \_ Stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ stat \_ maximal \_ Wert + 1\]**</span><span class="sxs-lookup"><span data-stu-id="5b430-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-127">Zusätzliche Bedrohungs Statistikdaten, z. b. die Anzahl der Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="5b430-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="5b430-128">Siehe [**mpthreat \_ Stats- \_ Daten**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="5b430-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b430-129">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="5b430-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-130">Typ: **[**mpcomponent- \_ Status**](mpcomponent-status.md) \[ mpcomponent \_ MaxValue + 1\]**</span><span class="sxs-lookup"><span data-stu-id="5b430-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-131">Ein Array von Status für mehrere Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5b430-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="5b430-132">Verwenden Sie einen Wert aus der [**mpcomponent- \_ ID**](mpcomponent-id.md) -Enumeration als Index in das Array.</span><span class="sxs-lookup"><span data-stu-id="5b430-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="5b430-133">**Productexpirationtime**</span><span class="sxs-lookup"><span data-stu-id="5b430-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="5b430-134">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="5b430-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="5b430-135">Zeitstempel für den Produktablauf in UNC.</span><span class="sxs-lookup"><span data-stu-id="5b430-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="5b430-136">Dies ist nur gültig, wenn der Ablauf Status auf festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b430-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b430-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b430-137">Requirements</span></span>



| <span data-ttu-id="5b430-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b430-138">Requirement</span></span> | <span data-ttu-id="5b430-139">Wert</span><span class="sxs-lookup"><span data-stu-id="5b430-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b430-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b430-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5b430-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b430-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5b430-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b430-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5b430-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b430-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b430-144">Header</span><span class="sxs-lookup"><span data-stu-id="5b430-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b430-145"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b430-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b430-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b430-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b430-147">**mpcomponent- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="5b430-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="5b430-148">**mpcomponent- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="5b430-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="5b430-149">**mpscan- \_ Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="5b430-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="5b430-150">**\_mpstatusflag**</span><span class="sxs-lookup"><span data-stu-id="5b430-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="5b430-151">**mpthreat- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="5b430-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="5b430-152">**mpthreat- \_ Statistik \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="5b430-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





