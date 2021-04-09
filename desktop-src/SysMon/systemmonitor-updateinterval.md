---
title: Systemmonitor. updateingeterval (Eigenschaft)
description: Ruft den Zeitraum ab oder legt den Zeitraum fest, den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Updateingeterval-Eigenschaft (Sysmon)
- Updateingeterval-Eigenschaft sysmon, Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, updateingeterval (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949801"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="36b97-106">Systemmonitor. updateingeterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="36b97-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="36b97-107">Ruft den Zeitraum ab oder legt den Zeitraum fest, den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="36b97-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="36b97-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="36b97-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b97-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="36b97-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="36b97-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="36b97-110">Property value</span></span>

<span data-ttu-id="36b97-111">Zeitraum (in Sekunden), den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="36b97-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="36b97-112">Das minimale Intervall beträgt 1 Sekunde (Dies ist auch der Standardwert).</span><span class="sxs-lookup"><span data-stu-id="36b97-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="36b97-113">Der Höchstwert ist 1 Million.</span><span class="sxs-lookup"><span data-stu-id="36b97-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b97-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36b97-114">Remarks</span></span>

<span data-ttu-id="36b97-115">Diese Eigenschaft ist nur relevant, wenn [**Systemmonitor. ManualUpdate**](systemmonitor-manualupdate.md) auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36b97-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b97-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36b97-116">Requirements</span></span>



| <span data-ttu-id="36b97-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36b97-117">Requirement</span></span> | <span data-ttu-id="36b97-118">Wert</span><span class="sxs-lookup"><span data-stu-id="36b97-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36b97-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36b97-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36b97-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36b97-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="36b97-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36b97-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36b97-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36b97-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36b97-123">DLL</span><span class="sxs-lookup"><span data-stu-id="36b97-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36b97-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="36b97-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b97-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36b97-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b97-126">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="36b97-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





