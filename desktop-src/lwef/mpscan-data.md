---
title: MPSCAN_DATA Struktur (mpclient. h)
description: Überprüfen Sie die an den Rückruf übergebenen Daten.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479167"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="d4a9f-105">Mpscan- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="d4a9f-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="d4a9f-106">Überprüfen Sie die an den Rückruf übergebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="d4a9f-107">Diese Struktur enthält kumulative Bedrohungs-und Ressourcen Statistiken.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="d4a9f-108">Diese Stat-Felder sind immer gültig.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a9f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a9f-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="d4a9f-110">Member</span><span class="sxs-lookup"><span data-stu-id="d4a9f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4a9f-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9f-112">Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4a9f-113">Scantyp.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9f-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9f-115">Typ: **pmpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="d4a9f-116">Ressourceninformationen</span><span class="sxs-lookup"><span data-stu-id="d4a9f-116">Resource information.</span></span> <span data-ttu-id="d4a9f-117">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="d4a9f-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4a9f-118">**Resourcestats**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9f-119">Typ: **[ **mpresource- \_ Statistik**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4a9f-120">Ressourcenbezogene kumulative Statistiken.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9f-121">**Bedrohlich stats**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9f-122">Typ: **[ **mpthreat- \_ Statistik**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4a9f-123">Bedrohungs Statistik mit erfolgreichen Überprüfungs Vervollständigungen.</span><span class="sxs-lookup"><span data-stu-id="d4a9f-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4a9f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4a9f-124">Requirements</span></span>



| <span data-ttu-id="d4a9f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4a9f-125">Requirement</span></span> | <span data-ttu-id="d4a9f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a9f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a9f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4a9f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d4a9f-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4a9f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d4a9f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4a9f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d4a9f-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4a9f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4a9f-131">Header</span><span class="sxs-lookup"><span data-stu-id="d4a9f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4a9f-132"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a9f-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a9f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4a9f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a9f-134">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="d4a9f-135">**mpresource- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="d4a9f-136">**mpscan- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="d4a9f-137">**mpthreat- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="d4a9f-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





