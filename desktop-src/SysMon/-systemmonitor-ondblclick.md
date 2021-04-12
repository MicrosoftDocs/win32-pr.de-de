---
title: System Monitor. OnDblClick-Ereignis
description: Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagramm Linie, die Histogrammleiste oder das Berichts Element doppelklickt.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- OnDblClick-Ereignis (Sysmon)
- OnDblClick-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", OnDblClick-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103838"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="4f091-106">System Monitor. OnDblClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f091-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="4f091-107">Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagramm Linie, die Histogrammleiste oder das Berichts Element doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="4f091-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f091-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f091-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="4f091-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f091-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f091-110">*Index* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4f091-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f091-111">Index des ausgewählten Indikators im [**indikatorensammlungs Objekt**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="4f091-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="4f091-112">Wenn kein Indikator ausgewählt wurde, wird der Indexwert 0 zurückgegeben. Andernfalls wird der Index des ausgewählten Zählers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f091-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f091-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f091-113">Return value</span></span>

<span data-ttu-id="4f091-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4f091-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f091-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f091-115">Remarks</span></span>

<span data-ttu-id="4f091-116">Wenn dieses Ereignis ausgelöst wird, wird der vom Benutzer im Liniendiagramm und im Histogramm ausgewählte Wert auch im Legenden Bereich ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4f091-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="4f091-117">Dies erleichtert es dem Benutzer des System Monitors, festzustellen, welcher Indikatoren ausgewählt wird, wenn mehrere Werte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4f091-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f091-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f091-118">Requirements</span></span>



| <span data-ttu-id="4f091-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f091-119">Requirement</span></span> | <span data-ttu-id="4f091-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4f091-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f091-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f091-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f091-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f091-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4f091-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f091-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f091-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f091-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f091-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4f091-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f091-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4f091-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





