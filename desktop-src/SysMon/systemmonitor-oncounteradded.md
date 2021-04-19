---
title: Systemmonitor. oncounteradded-Ereignis
description: Benachrichtigt Sie, wenn der Zähler Sammlung ein Indikator hinzugefügt wird.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Oncounteradded-Ereignis-sysmon
- Oncounteradded-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, oncounteradded-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342427"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="2697c-106">Systemmonitor. oncounteradded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2697c-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="2697c-107">Benachrichtigt Sie, wenn der [**Zähler**](counters.md) Sammlung ein Indikator hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2697c-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2697c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2697c-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="2697c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2697c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2697c-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2697c-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2697c-111">Index des Indikators [**, der dem indikatorensammlungs Objekt**](counters.md) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2697c-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2697c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2697c-112">Return value</span></span>

<span data-ttu-id="2697c-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2697c-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2697c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2697c-114">Requirements</span></span>



| <span data-ttu-id="2697c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2697c-115">Requirement</span></span> | <span data-ttu-id="2697c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2697c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2697c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2697c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2697c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2697c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2697c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2697c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2697c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2697c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2697c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2697c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2697c-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2697c-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2697c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2697c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2697c-124">**Systemmonitor. oncounterdeleted**</span><span class="sxs-lookup"><span data-stu-id="2697c-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="2697c-125">**Systemmonitor. oncounterselected**</span><span class="sxs-lookup"><span data-stu-id="2697c-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





