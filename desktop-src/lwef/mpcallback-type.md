---
title: MPCALLBACK_TYPE-Enumeration (mpclient. h)
description: Mögliche Rückruf Typen.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPCALLBACK_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476122"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="dc4d0-105">Mpcallback- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="dc4d0-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="dc4d0-106">Mögliche Rückruf Typen.</span><span class="sxs-lookup"><span data-stu-id="dc4d0-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc4d0-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="dc4d0-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="dc4d0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dc4d0-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**mpcallback \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**mpcallback- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**mpcallback- \_ Bedrohung**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**mpcallback- \_ Scan**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**mpcallback \_ Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**mpcallback- \_ vorab Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**mpcallback- \_ sigupdate**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**mpcallback- \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**mpcallback \_ reserviert**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**mpcallback- \_ Konfigurations \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**mpcallback- \_ FastPath**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**mpcallback- \_ Produkt \_ Ablauf**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**mpcallback \_ NIS \_ private**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**mpcallback \_ -Integrität**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**mpcallback- \_ EndOf**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**mpcallback- \_ Malware Toast**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dc4d0-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**mpcallback- \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="dc4d0-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="dc4d0-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc4d0-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dc4d0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc4d0-127">Requirements</span></span>



| <span data-ttu-id="dc4d0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc4d0-128">Requirement</span></span> | <span data-ttu-id="dc4d0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dc4d0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4d0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc4d0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4d0-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc4d0-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dc4d0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc4d0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4d0-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc4d0-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc4d0-134">Header</span><span class="sxs-lookup"><span data-stu-id="dc4d0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4d0-135"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4d0-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





