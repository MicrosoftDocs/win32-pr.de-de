---
title: Tasksettings. restartinterval (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Restartinterval-Eigenschaft Taskplaner
- Restartinterval-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, restartinterval (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740424"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="803a5-106">Tasksettings. restartinterval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="803a5-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="803a5-107">Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="803a5-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="803a5-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="803a5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="803a5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="803a5-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="803a5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="803a5-110">Property value</span></span>

<span data-ttu-id="803a5-111">Ein-Wert, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="803a5-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="803a5-112">Wenn diese Eigenschaft festgelegt ist, muss auch die [**restartcount**](tasksettings-restartcount.md) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="803a5-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="803a5-113">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="803a5-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="803a5-114">Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="803a5-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="803a5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="803a5-115">Remarks</span></span>

<span data-ttu-id="803a5-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Interval**](taskschedulerschema-interval-restarttype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="803a5-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="803a5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="803a5-117">Requirements</span></span>



| <span data-ttu-id="803a5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="803a5-118">Requirement</span></span> | <span data-ttu-id="803a5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="803a5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="803a5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="803a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="803a5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="803a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="803a5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="803a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="803a5-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="803a5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="803a5-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="803a5-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="803a5-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="803a5-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="803a5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="803a5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="803a5-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803a5-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803a5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="803a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803a5-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="803a5-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





