---
title: MPTHREAT_DETECTION-Enumeration (mpclient. h)
description: Mögliche bekannte Typen fehlerhafter Bedrohungserkennung.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_DETECTION enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741008"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="766b1-105">Mpthreat- \_ Erkennungs Enumeration</span><span class="sxs-lookup"><span data-stu-id="766b1-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="766b1-106">Mögliche bekannte Typen fehlerhafter Bedrohungserkennung.</span><span class="sxs-lookup"><span data-stu-id="766b1-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="766b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="766b1-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="766b1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="766b1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="766b1-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP- \_ Bedrohungs \_ Erkennung \_ konkret**</span><span class="sxs-lookup"><span data-stu-id="766b1-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="766b1-110">Die Bedrohung wurde über konkrete Signaturen erkannt.</span><span class="sxs-lookup"><span data-stu-id="766b1-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="766b1-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP- \_ Bedrohungs \_ Erkennung \_ heuristic**</span><span class="sxs-lookup"><span data-stu-id="766b1-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="766b1-112">Die Bedrohung wurde über eine Heuristik erkannt.</span><span class="sxs-lookup"><span data-stu-id="766b1-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="766b1-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP- \_ Bedrohungs \_ Erkennung \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="766b1-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="766b1-114">Die Bedrohung wurde über generische Signaturen erkannt.</span><span class="sxs-lookup"><span data-stu-id="766b1-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="766b1-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP- \_ Bedrohungs \_ Erkennung \_ verdächtig**</span><span class="sxs-lookup"><span data-stu-id="766b1-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="766b1-116">Die Bedrohungserkennung wurde durch die Verhaltens Überwachung erkannt.</span><span class="sxs-lookup"><span data-stu-id="766b1-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="766b1-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP- \_ Bedrohungs \_ Erkennung \_ FastPath**</span><span class="sxs-lookup"><span data-stu-id="766b1-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="766b1-118">Die Bedrohung wurde über FastPath erkannt.</span><span class="sxs-lookup"><span data-stu-id="766b1-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="766b1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="766b1-119">Requirements</span></span>



| <span data-ttu-id="766b1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="766b1-120">Requirement</span></span> | <span data-ttu-id="766b1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="766b1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="766b1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="766b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="766b1-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="766b1-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="766b1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="766b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="766b1-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="766b1-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="766b1-126">Header</span><span class="sxs-lookup"><span data-stu-id="766b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="766b1-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="766b1-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





