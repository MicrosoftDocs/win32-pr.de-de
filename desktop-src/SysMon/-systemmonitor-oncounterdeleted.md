---
title: Systemmonitor. oncounterdeleted-Ereignis
description: Benachrichtigt Sie, bevor ein Indikator aus der Zähler Sammlung gelöscht wird.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Oncounterdeleted-Ereignis (Sysmon)
- Oncounterdeleted-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", oncounterdeleted-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956521"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="134e5-106">Systemmonitor. oncounterdeleted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="134e5-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="134e5-107">Benachrichtigt Sie, bevor ein Indikator aus der [**Zähler**](counters.md) Sammlung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="134e5-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="134e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="134e5-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="134e5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="134e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="134e5-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="134e5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134e5-111">Index des Indikators [**, der aus**](counters.md) dem indikatorensammlungs Objekt gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="134e5-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="134e5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="134e5-112">Return value</span></span>

<span data-ttu-id="134e5-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="134e5-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="134e5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="134e5-114">Requirements</span></span>



| <span data-ttu-id="134e5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="134e5-115">Requirement</span></span> | <span data-ttu-id="134e5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="134e5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="134e5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="134e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="134e5-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="134e5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="134e5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="134e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="134e5-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="134e5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="134e5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="134e5-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="134e5-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="134e5-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="134e5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="134e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134e5-124">**Systemmonitor. oncounteradded**</span><span class="sxs-lookup"><span data-stu-id="134e5-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="134e5-125">**Systemmonitor. oncounterselected**</span><span class="sxs-lookup"><span data-stu-id="134e5-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





