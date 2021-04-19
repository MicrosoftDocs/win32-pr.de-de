---
title: Hidden (settingstype)-Element
description: Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Hidden-Element Taskplaner
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344722"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="1e9e3-104">Hidden (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="1e9e3-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="1e9e3-105">Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9e3-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="1e9e3-106">Administratoren können diese Einstellung jedoch überschreiben, indem Sie einen "Master Switch" verwenden, der alle Aufgaben in der Benutzeroberfläche sichtbar macht.</span><span class="sxs-lookup"><span data-stu-id="1e9e3-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="1e9e3-107">Das **Hidden** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="1e9e3-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1e9e3-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1e9e3-108">Parent element</span></span>



| <span data-ttu-id="1e9e3-109">Element</span><span class="sxs-lookup"><span data-stu-id="1e9e3-109">Element</span></span>                                                           | <span data-ttu-id="1e9e3-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="1e9e3-110">Derived from</span></span>                                                         | <span data-ttu-id="1e9e3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e9e3-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="1e9e3-112">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="1e9e3-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1e9e3-113">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="1e9e3-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1e9e3-114">Enthält die Einstellungen, die Taskplaner verwendet, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1e9e3-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e9e3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e9e3-115">Remarks</span></span>

<span data-ttu-id="1e9e3-116">Informationen zur C++-Entwicklung finden Sie unter [**Hidden-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="1e9e3-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="1e9e3-117">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="1e9e3-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9e3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e9e3-118">Requirements</span></span>



| <span data-ttu-id="1e9e3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e9e3-119">Requirement</span></span> | <span data-ttu-id="1e9e3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9e3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e9e3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e9e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9e3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9e3-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e9e3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e9e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9e3-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9e3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e9e3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e9e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9e3-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="1e9e3-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





