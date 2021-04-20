---
title: TaskSettings.RestartInterval-Eigenschaft
description: Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- RestartInterval-Eigenschaft Taskplaner
- RestartInterval-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , RestartInterval-Eigenschaft
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
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734145"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="51cec-106">TaskSettings.RestartInterval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51cec-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="51cec-107">Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="51cec-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="51cec-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="51cec-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="51cec-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="51cec-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="51cec-110">Property value</span></span>

<span data-ttu-id="51cec-111">Ein -Wert, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="51cec-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="51cec-112">Wenn diese Eigenschaft festgelegt ist, muss auch die [**RestartCount-Eigenschaft**](tasksettings-restartcount.md) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51cec-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="51cec-113">Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (z. B. "PT5M" ist 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" ist 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="51cec-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="51cec-114">Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="51cec-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="51cec-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51cec-115">Remarks</span></span>

<span data-ttu-id="51cec-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Interval-Element**](taskschedulerschema-interval-restarttype-element.md) des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="51cec-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cec-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51cec-117">Requirements</span></span>



| <span data-ttu-id="51cec-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51cec-118">Requirement</span></span> | <span data-ttu-id="51cec-119">Wert</span><span class="sxs-lookup"><span data-stu-id="51cec-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51cec-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51cec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51cec-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51cec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="51cec-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51cec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51cec-123">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51cec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51cec-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="51cec-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="51cec-125"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="51cec-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="51cec-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51cec-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51cec-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51cec-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51cec-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51cec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cec-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="51cec-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





