---
title: Systemmonitor. monitordupli-Einhaltungen (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Leistungsindikators überwacht werden können, oder legt ihn fest.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Monitordupliplateinhaltungen-Eigenschaft (Sysmon)
- Monitordupliplateinhaltungen-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", monitordupliplateinhaltungen (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391810"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="eaad3-106">Systemmonitor. monitordupli-Einhaltungen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="eaad3-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="eaad3-107">Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Leistungsindikators überwacht werden können, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="eaad3-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="eaad3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="eaad3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaad3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaad3-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="eaad3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eaad3-110">Property value</span></span>

<span data-ttu-id="eaad3-111">True gibt an, dass mehrere Instanzen eines Zählers überwacht werden können ("true" ist die Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="eaad3-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="eaad3-112">False gibt an, dass nur eine Instanz eines Zählers überwacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="eaad3-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaad3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaad3-113">Remarks</span></span>

<span data-ttu-id="eaad3-114">Der System Monitor fügt \# n an jeden Instanznamen an, mit Ausnahme des ersten, wenn mehrere Instanzen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eaad3-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="eaad3-115">Die Seriennummer n beginnt mit einem und wird für jede neue Instanz um eins erhöht.</span><span class="sxs-lookup"><span data-stu-id="eaad3-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="eaad3-116">Wenn Sie z. b. " \\ Process ( \* ) \\ % Processor Time" angeben, sollte die zählungssammlung mehrere Instanzen von svchost enthalten.</span><span class="sxs-lookup"><span data-stu-id="eaad3-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="eaad3-117">Das erste Vorkommen ist svchost, das nächste Vorkommen lautet svchost \# 1 usw.</span><span class="sxs-lookup"><span data-stu-id="eaad3-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="eaad3-118">Doppelte Instanzen werden nur überwacht, wenn Sie das Platzhalter Zeichen ( \* ) für den Instanznamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="eaad3-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="eaad3-119">Wenn Sie " \\ Process (SVCHOST) \\ % Processor Time" angegeben haben, wird nur die erste Instanz von svchost überwacht, nicht alle Instanzen von svchost.</span><span class="sxs-lookup"><span data-stu-id="eaad3-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaad3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaad3-120">Requirements</span></span>



| <span data-ttu-id="eaad3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaad3-121">Requirement</span></span> | <span data-ttu-id="eaad3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="eaad3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaad3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaad3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eaad3-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaad3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eaad3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaad3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eaad3-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaad3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaad3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eaad3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaad3-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="eaad3-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaad3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaad3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaad3-130">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="eaad3-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





