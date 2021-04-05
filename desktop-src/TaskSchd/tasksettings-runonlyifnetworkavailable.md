---
title: Tasksettings. runonlyifnetworkavailable (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Runonlyifnetworkavailable-Eigenschaft Taskplaner
- Runonlyifnetworkavailable-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, runonlyifnetworkavailable-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859138"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="5b140-106">Tasksettings. runonlyifnetworkavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b140-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="5b140-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="5b140-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="5b140-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5b140-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b140-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b140-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5b140-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5b140-110">Property value</span></span>

<span data-ttu-id="5b140-111">Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn ein Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5b140-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="5b140-112">Die Standardeinstellung lautet „false“.</span><span class="sxs-lookup"><span data-stu-id="5b140-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b140-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b140-113">Remarks</span></span>

<span data-ttu-id="5b140-114">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="5b140-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b140-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b140-115">Requirements</span></span>



| <span data-ttu-id="5b140-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b140-116">Requirement</span></span> | <span data-ttu-id="5b140-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5b140-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b140-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b140-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5b140-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b140-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5b140-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b140-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5b140-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b140-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b140-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5b140-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b140-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b140-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b140-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5b140-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b140-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b140-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b140-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b140-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b140-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="5b140-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





