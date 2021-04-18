---
title: MPTHREAT_SEVERITY-Enumeration (mpclient. h)
description: Mögliche Bedrohungs Schweregrade.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_SEVERITY enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339149"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="8fc85-105">Mpthreat- \_ Schweregrad Enumeration</span><span class="sxs-lookup"><span data-stu-id="8fc85-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="8fc85-106">Mögliche Bedrohungs Schweregrade.</span><span class="sxs-lookup"><span data-stu-id="8fc85-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc85-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc85-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="8fc85-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8fc85-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8fc85-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP- \_ Bedrohungs \_ Schweregrad \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="8fc85-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fc85-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP- \_ Bedrohungs \_ Schweregrad \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="8fc85-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fc85-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**Management Pack- \_ Bedrohungs \_ Schweregrad \_**</span><span class="sxs-lookup"><span data-stu-id="8fc85-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fc85-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP- \_ Bedrohungs \_ Schweregrad \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="8fc85-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fc85-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**Management Pack- \_ Bedrohungs schwere \_ Grad \_**</span><span class="sxs-lookup"><span data-stu-id="8fc85-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fc85-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP- \_ Bedrohungs \_ Schweregrad \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="8fc85-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="8fc85-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fc85-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8fc85-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fc85-116">Requirements</span></span>



| <span data-ttu-id="8fc85-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fc85-117">Requirement</span></span> | <span data-ttu-id="8fc85-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8fc85-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc85-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fc85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc85-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fc85-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8fc85-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fc85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc85-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fc85-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fc85-123">Header</span><span class="sxs-lookup"><span data-stu-id="8fc85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc85-124"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc85-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





