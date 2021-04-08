---
title: Tasksettings. Hidden (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe in der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Taskplaner für verborgene Eigenschaften
- Ausgeblendete Eigenschaften Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Hidden-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742737"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="8891f-106">Tasksettings. Hidden (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8891f-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="8891f-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe in der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="8891f-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="8891f-108">Administratoren können diese Einstellung jedoch überschreiben, indem Sie einen "Master Switch" verwenden, der alle Aufgaben in der Benutzeroberfläche sichtbar macht.</span><span class="sxs-lookup"><span data-stu-id="8891f-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="8891f-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8891f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8891f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8891f-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8891f-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8891f-111">Property value</span></span>

<span data-ttu-id="8891f-112">Wenn der Wert **true** ist, gibt der Wert an, dass die Aufgabe nicht in der Benutzeroberfläche sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="8891f-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="8891f-113">Wenn der Wert **false** ist, wird die Aufgabe in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8891f-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="8891f-114">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="8891f-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8891f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8891f-115">Remarks</span></span>

<span data-ttu-id="8891f-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Hidden-Element [**(settingstype)**](taskschedulerschema-hidden-settingstype-element.md) des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="8891f-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8891f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8891f-117">Requirements</span></span>



| <span data-ttu-id="8891f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8891f-118">Requirement</span></span> | <span data-ttu-id="8891f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8891f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8891f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8891f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8891f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8891f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8891f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8891f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8891f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8891f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8891f-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8891f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8891f-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8891f-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8891f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8891f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8891f-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8891f-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8891f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8891f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8891f-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8891f-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





