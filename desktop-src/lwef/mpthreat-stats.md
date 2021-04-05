---
title: MPTHREAT_STATS Struktur (mpclient. h)
description: Bedrohungs bezogene Statistiken.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_STATS Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858858"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="2fb2d-105">Mpthreat \_ Stats-Struktur</span><span class="sxs-lookup"><span data-stu-id="2fb2d-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="2fb2d-106">Bedrohungs bezogene Statistiken.</span><span class="sxs-lookup"><span data-stu-id="2fb2d-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb2d-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="2fb2d-108">Member</span><span class="sxs-lookup"><span data-stu-id="2fb2d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fb2d-109">**Anzahl von Zustellungen**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="2fb2d-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="2fb2d-111">Anzahl der erkannten Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="2fb2d-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="2fb2d-112">**Verdächtiger Anzahl**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="2fb2d-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="2fb2d-114">Anzahl der erkannten Bedrohungen bei der Verhaltens Überwachung.</span><span class="sxs-lookup"><span data-stu-id="2fb2d-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="2fb2d-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2fb2d-116">Typ: **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="2fb2d-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="2fb2d-117">Felder, die für die zukünftige Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="2fb2d-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fb2d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fb2d-118">Requirements</span></span>



| <span data-ttu-id="2fb2d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fb2d-119">Requirement</span></span> | <span data-ttu-id="2fb2d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2fb2d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb2d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fb2d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb2d-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fb2d-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2fb2d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fb2d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb2d-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fb2d-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fb2d-125">Header</span><span class="sxs-lookup"><span data-stu-id="2fb2d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb2d-126"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb2d-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





