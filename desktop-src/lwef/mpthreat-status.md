---
title: MPTHREAT_STATUS-Enumeration (mpclient. h)
description: Möglicher Bedrohungs Status.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_STATUS enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339954"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="9a7c2-105">Mpthreat- \_ statusenumeration</span><span class="sxs-lookup"><span data-stu-id="9a7c2-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="9a7c2-106">Möglicher Bedrohungs Status.</span><span class="sxs-lookup"><span data-stu-id="9a7c2-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a7c2-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="9a7c2-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9a7c2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9a7c2-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP- \_ Bedrohungs \_ Status \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP- \_ Bedrohungs \_ Status \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**Management Pack- \_ Bedrohungs \_ Status \_ bereinigt**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP- \_ Bedrohungs \_ Status unter \_ Quarantäne**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP- \_ Bedrohungs \_ Status \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP- \_ Bedrohungs \_ Status \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP- \_ Bedrohungs \_ Status \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**Fehler \_ beim \_ \_ Bereinigen des Management Packs. \_**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**Fehler bei MP- \_ Bedrohungs \_ Status \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**Fehler \_ beim \_ \_ Entfernen \_ des Management Packs.**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**Fehler bei MP- \_ Bedrohungs \_ Status \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP- \_ Bedrohungs \_ Status \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9a7c2-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**Fehler beim MP- \_ Bedrohungs \_ Status. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="9a7c2-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9a7c2-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9a7c2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a7c2-123">Requirements</span></span>



| <span data-ttu-id="9a7c2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a7c2-124">Requirement</span></span> | <span data-ttu-id="9a7c2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9a7c2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7c2-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a7c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7c2-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a7c2-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9a7c2-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a7c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7c2-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a7c2-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a7c2-130">Header</span><span class="sxs-lookup"><span data-stu-id="9a7c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7c2-131"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c2-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





