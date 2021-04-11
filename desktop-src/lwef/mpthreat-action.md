---
title: MPTHREAT_ACTION-Enumeration (mpclient. h)
description: Mögliche Bedrohungs Aktionen.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_ACTION enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103562"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="e7a01-105">Mpthreat \_ Action-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e7a01-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="e7a01-106">Mögliche Bedrohungs Aktionen.</span><span class="sxs-lookup"><span data-stu-id="e7a01-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7a01-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="e7a01-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e7a01-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e7a01-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP- \_ Bedrohungs \_ Aktion \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="e7a01-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**Management Pack- \_ Bedrohungs \_ Aktion \_ bereinigt**</span><span class="sxs-lookup"><span data-stu-id="e7a01-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_Quarantäne mit Bedrohungs \_ Aktion \_**</span><span class="sxs-lookup"><span data-stu-id="e7a01-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP- \_ Bedrohungs \_ Aktion \_ Entfernen**</span><span class="sxs-lookup"><span data-stu-id="e7a01-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP- \_ Bedrohungs \_ Aktion \_ zulassen**</span><span class="sxs-lookup"><span data-stu-id="e7a01-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP- \_ Bedrohungs \_ Aktion \_ UserDefined**</span><span class="sxs-lookup"><span data-stu-id="e7a01-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP- \_ Bedrohungs \_ Aktion \_ NoAction**</span><span class="sxs-lookup"><span data-stu-id="e7a01-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP- \_ Bedrohungs \_ Aktions \_ Block**</span><span class="sxs-lookup"><span data-stu-id="e7a01-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e7a01-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**Maximalwert für MP- \_ Bedrohungs \_ Aktion \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7a01-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="e7a01-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e7a01-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e7a01-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7a01-119">Requirements</span></span>



| <span data-ttu-id="e7a01-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7a01-120">Requirement</span></span> | <span data-ttu-id="e7a01-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a01-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a01-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7a01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a01-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a01-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e7a01-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7a01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a01-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a01-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7a01-126">Header</span><span class="sxs-lookup"><span data-stu-id="e7a01-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a01-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a01-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





