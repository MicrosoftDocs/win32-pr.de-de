---
title: MPSCAN_RESULT Struktur (mpclient. h)
description: Die Ergebnisse einer Überprüfung.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_RESULT Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213746"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="81357-105">Mpscan- \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="81357-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="81357-106">Die Ergebnisse einer Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="81357-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="81357-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81357-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="81357-108">Member</span><span class="sxs-lookup"><span data-stu-id="81357-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="81357-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="81357-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="81357-110">Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="81357-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81357-111">Scantyp.</span><span class="sxs-lookup"><span data-stu-id="81357-111">Scan type.</span></span> <span data-ttu-id="81357-112">Siehe [**mpscan- \_ Typ**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="81357-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="81357-113">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="81357-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="81357-114">Typ: **[ **mpsource**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="81357-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81357-115">Scan Quelle, z. b. Benutzer oder System initiiert.</span><span class="sxs-lookup"><span data-stu-id="81357-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="81357-116">Siehe [**mpsource**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="81357-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="81357-117">**Scanguid**</span><span class="sxs-lookup"><span data-stu-id="81357-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="81357-118">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="81357-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="81357-119">Scan Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="81357-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="81357-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="81357-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="81357-121">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="81357-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="81357-122">Startzeitpunkt der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="81357-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="81357-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="81357-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="81357-124">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="81357-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="81357-125">Endzeit des Scan Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="81357-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="81357-126">**Bedrohlich stats**</span><span class="sxs-lookup"><span data-stu-id="81357-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="81357-127">Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="81357-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81357-128">Bedrohungs bezogene Statistiken.</span><span class="sxs-lookup"><span data-stu-id="81357-128">Threat-related statistics.</span></span> <span data-ttu-id="81357-129">Siehe [**mpthreat \_ Stats**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="81357-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="81357-130">**Resourcestats**</span><span class="sxs-lookup"><span data-stu-id="81357-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="81357-131">Typ: **[ **mpresource- \_ Statistik**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="81357-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81357-132">Ressourcenbezogene Statistiken.</span><span class="sxs-lookup"><span data-stu-id="81357-132">Resource-related statistics.</span></span> <span data-ttu-id="81357-133">Siehe [**mpresource- \_ Statistik**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="81357-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="81357-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="81357-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="81357-135">Typ: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="81357-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="81357-136">Version der Signatur, die für die Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81357-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81357-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81357-137">Requirements</span></span>



| <span data-ttu-id="81357-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81357-138">Requirement</span></span> | <span data-ttu-id="81357-139">Wert</span><span class="sxs-lookup"><span data-stu-id="81357-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81357-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81357-140">Minimum supported client</span></span><br/> | <span data-ttu-id="81357-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81357-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="81357-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81357-142">Minimum supported server</span></span><br/> | <span data-ttu-id="81357-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81357-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81357-144">Header</span><span class="sxs-lookup"><span data-stu-id="81357-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="81357-145"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="81357-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81357-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81357-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81357-147">**mpresource- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="81357-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="81357-148">**mpscan- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="81357-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="81357-149">**Mpsource**</span><span class="sxs-lookup"><span data-stu-id="81357-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="81357-150">**mpthreat- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="81357-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





