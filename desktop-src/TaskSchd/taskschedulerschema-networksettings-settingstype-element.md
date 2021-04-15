---
title: Network Settings (settingstype)-Element
description: Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das runonlyifnetworkavailable-Element auf "true" festgelegt ist.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Network settings-Element Taskplaner
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477463"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="60005-105">Network Settings (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="60005-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="60005-106">Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60005-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="60005-107">Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60005-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="60005-108">Das **networksettings** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="60005-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="60005-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="60005-109">Parent element</span></span>



| <span data-ttu-id="60005-110">Element</span><span class="sxs-lookup"><span data-stu-id="60005-110">Element</span></span>                                                                      | <span data-ttu-id="60005-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="60005-111">Derived from</span></span>                                                         | <span data-ttu-id="60005-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60005-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="60005-113">**Einstellungen (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="60005-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="60005-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="60005-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="60005-115">Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60005-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60005-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60005-116">Remarks</span></span>

<span data-ttu-id="60005-117">Informationen zur C++-Entwicklung finden Sie unter [**networksettings-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="60005-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="60005-118">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. networksettings**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="60005-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60005-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60005-119">Requirements</span></span>



| <span data-ttu-id="60005-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60005-120">Requirement</span></span> | <span data-ttu-id="60005-121">Wert</span><span class="sxs-lookup"><span data-stu-id="60005-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60005-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60005-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60005-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60005-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60005-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60005-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60005-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60005-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





