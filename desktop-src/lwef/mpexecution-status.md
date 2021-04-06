---
title: MPEXECUTION_STATUS-Enumeration (mpclient. h)
description: Möglicher Bedrohungs Ausführungs Status.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPEXECUTION_STATUS enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858792"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="c50e1-105">Mpexecution- \_ statusenumeration</span><span class="sxs-lookup"><span data-stu-id="c50e1-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="c50e1-106">Möglicher Bedrohungs Ausführungs Status.</span><span class="sxs-lookup"><span data-stu-id="c50e1-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c50e1-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="c50e1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c50e1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c50e1-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP- \_ Ausführungs \_ Status \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="c50e1-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c50e1-110">Der Ausführungs Status ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="c50e1-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP- \_ Ausführungs \_ Status \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="c50e1-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="c50e1-112">Die Ausführung durch den Mini Filter wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="c50e1-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP- \_ Ausführungs \_ Status \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="c50e1-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="c50e1-114">Die Ausführung durch den Mini Filter ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="c50e1-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**Ausführungs Status von MP wird \_ \_ \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="c50e1-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="c50e1-116">Die Bedrohung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c50e1-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP- \_ Ausführungs \_ Status wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="c50e1-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="c50e1-118">Die Bedrohung wird nicht ausgeführt und ist nur während der Wiederherstellung über die Engine verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c50e1-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c50e1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c50e1-119">Requirements</span></span>



| <span data-ttu-id="c50e1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c50e1-120">Requirement</span></span> | <span data-ttu-id="c50e1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c50e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c50e1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c50e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c50e1-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c50e1-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c50e1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c50e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c50e1-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c50e1-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c50e1-126">Header</span><span class="sxs-lookup"><span data-stu-id="c50e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50e1-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50e1-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





