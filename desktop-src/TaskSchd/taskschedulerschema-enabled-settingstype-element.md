---
title: Aktiviertes (settingstype)-Element
description: Gibt an, dass der Task aktiviert ist. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Aktiviertes Element Taskplaner
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340372"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="79e6f-105">Aktiviertes (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="79e6f-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="79e6f-106">Gibt an, dass der Task aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79e6f-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="79e6f-107">Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79e6f-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="79e6f-108">Das **aktivierte** Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="79e6f-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="79e6f-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="79e6f-109">Parent element</span></span>



| <span data-ttu-id="79e6f-110">Element</span><span class="sxs-lookup"><span data-stu-id="79e6f-110">Element</span></span>                                                           | <span data-ttu-id="79e6f-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="79e6f-111">Derived from</span></span>                                                         | <span data-ttu-id="79e6f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e6f-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="79e6f-113">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="79e6f-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="79e6f-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="79e6f-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="79e6f-115">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="79e6f-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="79e6f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79e6f-116">Remarks</span></span>

<span data-ttu-id="79e6f-117">Informationen zur C++-Entwicklung finden Sie unter [**aktivierte Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="79e6f-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="79e6f-118">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. aktiviert**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="79e6f-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="79e6f-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79e6f-119">Examples</span></span>

<span data-ttu-id="79e6f-120">Ein umfassendes Beispiel für den XML-Code für eine aktivierte Aufgabe finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="79e6f-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e6f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79e6f-121">Requirements</span></span>



| <span data-ttu-id="79e6f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79e6f-122">Requirement</span></span> | <span data-ttu-id="79e6f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="79e6f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79e6f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79e6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79e6f-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79e6f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79e6f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79e6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79e6f-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79e6f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





