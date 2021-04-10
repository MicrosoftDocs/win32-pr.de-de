---
title: MPTHREAT_STATS_DATA Struktur (mpclient. h)
description: Zusätzliche Bedrohungs Statistikdaten.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_STATS_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103559"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="aedc7-105">Mpthreat \_ Stats- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="aedc7-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="aedc7-106">Zusätzliche Bedrohungs Statistikdaten.</span><span class="sxs-lookup"><span data-stu-id="aedc7-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="aedc7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aedc7-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="aedc7-108">Member</span><span class="sxs-lookup"><span data-stu-id="aedc7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="aedc7-109">**dwercount**</span><span class="sxs-lookup"><span data-stu-id="aedc7-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="aedc7-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="aedc7-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="aedc7-111">Anzahl der Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="aedc7-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aedc7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aedc7-112">Requirements</span></span>



| <span data-ttu-id="aedc7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aedc7-113">Requirement</span></span> | <span data-ttu-id="aedc7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="aedc7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aedc7-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aedc7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aedc7-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aedc7-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aedc7-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aedc7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aedc7-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aedc7-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aedc7-119">Header</span><span class="sxs-lookup"><span data-stu-id="aedc7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="aedc7-120"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="aedc7-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





