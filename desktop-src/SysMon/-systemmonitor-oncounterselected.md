---
title: Systemmonitor. oncounterselected-Ereignis
description: Benachrichtigt Sie, wenn ein Counter ausgewählt wird.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Oncounterselected-Ereignis (Sysmon)
- Oncounterselected-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", oncounterselected-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342439"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="46fb8-106">Systemmonitor. oncounterselected-Ereignis</span><span class="sxs-lookup"><span data-stu-id="46fb8-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="46fb8-107">Benachrichtigt Sie, wenn ein Counter ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="46fb8-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fb8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46fb8-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="46fb8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46fb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46fb8-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46fb8-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46fb8-111">Index des ausgewählten Indikators im [**indikatorensammlungs Objekt**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="46fb8-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46fb8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46fb8-112">Return value</span></span>

<span data-ttu-id="46fb8-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46fb8-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46fb8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46fb8-114">Remarks</span></span>

<span data-ttu-id="46fb8-115">Sie können dieses Ereignis empfangen, wenn</span><span class="sxs-lookup"><span data-stu-id="46fb8-115">You can receive this event when</span></span>

-   <span data-ttu-id="46fb8-116">Sie legen " [**count Item. Selected**](counteritem-selected.md) " auf "true" fest.</span><span class="sxs-lookup"><span data-stu-id="46fb8-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="46fb8-117">Der Benutzer wählt einen gegen Wert in der Legende aus.</span><span class="sxs-lookup"><span data-stu-id="46fb8-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="46fb8-118">Der Benutzer doppelklickt auf einen Gegenstand in der Legende.</span><span class="sxs-lookup"><span data-stu-id="46fb8-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="46fb8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46fb8-119">Requirements</span></span>



| <span data-ttu-id="46fb8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46fb8-120">Requirement</span></span> | <span data-ttu-id="46fb8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="46fb8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46fb8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46fb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46fb8-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46fb8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="46fb8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46fb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46fb8-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46fb8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46fb8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="46fb8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46fb8-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="46fb8-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46fb8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46fb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fb8-129">**Systemmonitor. oncounteradded**</span><span class="sxs-lookup"><span data-stu-id="46fb8-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="46fb8-130">**Systemmonitor. oncounterdeleted**</span><span class="sxs-lookup"><span data-stu-id="46fb8-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





