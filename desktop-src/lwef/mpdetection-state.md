---
title: MPDETECTION_STATE-Enumeration (mpclient. h)
description: Der Status der aktuell erkannten Bedrohung.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPDETECTION_STATE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476113"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="48b73-105">Mperkennungs- \_ statusenumeration</span><span class="sxs-lookup"><span data-stu-id="48b73-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="48b73-106">Der Status der aktuell erkannten Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="48b73-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b73-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b73-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="48b73-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="48b73-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48b73-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Unbekannter mperkennungs- \_ Zustand. \_**</span><span class="sxs-lookup"><span data-stu-id="48b73-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-110">In einem Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="48b73-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**mperkennungs- \_ Status \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="48b73-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-112">Aktive Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="48b73-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**mperkennungs- \_ Status \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="48b73-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-114">Ausstehende 24 Stunden bis zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="48b73-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**mperkennungs \_ Status \_ zusätzliche \_ Aktionen**</span><span class="sxs-lookup"><span data-stu-id="48b73-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-116">Weitere erforderliche Aktionen.</span><span class="sxs-lookup"><span data-stu-id="48b73-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**mperkennungs- \_ Status ist \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="48b73-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-118">Nicht schwerwiegender Fehler bei der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="48b73-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**Fehler beim mperkennungs \_ Zustand. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48b73-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-120">Kritischer Fehler bei der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="48b73-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="48b73-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**mperkennungs- \_ Status \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="48b73-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="48b73-122">Die Bedrohung wird in der Zustands Abfrage nicht angezeigt, sondern nur im Verlauf.</span><span class="sxs-lookup"><span data-stu-id="48b73-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48b73-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b73-123">Requirements</span></span>



| <span data-ttu-id="48b73-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b73-124">Requirement</span></span> | <span data-ttu-id="48b73-125">Wert</span><span class="sxs-lookup"><span data-stu-id="48b73-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48b73-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48b73-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b73-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="48b73-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48b73-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b73-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48b73-130">Header</span><span class="sxs-lookup"><span data-stu-id="48b73-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b73-131"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b73-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





