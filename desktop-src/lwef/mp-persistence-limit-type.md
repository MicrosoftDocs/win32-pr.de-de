---
title: MP_PERSISTENCE_LIMIT_TYPE-Enumeration (mpclient. h)
description: Typ der Dauerhaftigkeits Beschränkung.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMP_PERSISTENCE_LIMIT_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040920"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="12a02-105">MP \_ - \_ persistenzlimit- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="12a02-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="12a02-106">Typ der Dauerhaftigkeits Beschränkung.</span><span class="sxs-lookup"><span data-stu-id="12a02-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a02-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a02-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="12a02-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12a02-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12a02-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP- \_ Persistenz \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="12a02-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-110">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="12a02-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="12a02-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP- \_ Persistenz ist \_ \_ unbegrenzt.**</span><span class="sxs-lookup"><span data-stu-id="12a02-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-112">Keine Begrenzung</span><span class="sxs-lookup"><span data-stu-id="12a02-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="12a02-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP \_ - \_ Dauerhaftigkeit**</span><span class="sxs-lookup"><span data-stu-id="12a02-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-114">Dauer.</span><span class="sxs-lookup"><span data-stu-id="12a02-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="12a02-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**Management Pack- \_ Persistenz- \_ VDM \_**</span><span class="sxs-lookup"><span data-stu-id="12a02-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-116">VDM-Version.</span><span class="sxs-lookup"><span data-stu-id="12a02-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="12a02-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP \_ - \_ persistenzzeit Stempel**</span><span class="sxs-lookup"><span data-stu-id="12a02-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-118">Timestamp.</span><span class="sxs-lookup"><span data-stu-id="12a02-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="12a02-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP- \_ Persistenz \_ erzwungen**</span><span class="sxs-lookup"><span data-stu-id="12a02-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="12a02-120">Erzwingen.</span><span class="sxs-lookup"><span data-stu-id="12a02-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12a02-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12a02-121">Requirements</span></span>



| <span data-ttu-id="12a02-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12a02-122">Requirement</span></span> | <span data-ttu-id="12a02-123">Wert</span><span class="sxs-lookup"><span data-stu-id="12a02-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12a02-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12a02-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12a02-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12a02-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="12a02-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12a02-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12a02-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12a02-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12a02-128">Header</span><span class="sxs-lookup"><span data-stu-id="12a02-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="12a02-129"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a02-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





