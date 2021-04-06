---
title: Networkprofilename (settingstype)-Element
description: Enthält den Namen eines Netzwerk Profils. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das runonlyifnetworkavailable-Element auf "true" festgelegt ist. Der Name wird zu Anzeige Zwecken verwendet.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Networkprofilename-Element Taskplaner
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742160"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="77415-106">Networkprofilename (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="77415-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="77415-107">Enthält den Namen eines Netzwerk Profils.</span><span class="sxs-lookup"><span data-stu-id="77415-107">Contains the name of a network profile.</span></span> <span data-ttu-id="77415-108">Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="77415-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="77415-109">Der Name wird zu Anzeige Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="77415-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="77415-110">Das **networkprofilename** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="77415-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="77415-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="77415-111">Parent element</span></span>



| <span data-ttu-id="77415-112">Element</span><span class="sxs-lookup"><span data-stu-id="77415-112">Element</span></span>                                                                      | <span data-ttu-id="77415-113">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="77415-113">Derived from</span></span>                                                         | <span data-ttu-id="77415-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77415-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="77415-115">**Einstellungen (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="77415-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="77415-116">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="77415-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="77415-117">Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77415-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="77415-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77415-118">Requirements</span></span>



| <span data-ttu-id="77415-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77415-119">Requirement</span></span> | <span data-ttu-id="77415-120">Wert</span><span class="sxs-lookup"><span data-stu-id="77415-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77415-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77415-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77415-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77415-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77415-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77415-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77415-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77415-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





