---
title: Name (networksettingstype)-Element
description: Enthält den Namen eines Netzwerk Profils. Der Name wird zu Anzeige Zwecken verwendet.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name-Element Taskplaner
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518071"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="5259a-105">Name (networksettingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="5259a-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="5259a-106">Enthält den Namen eines Netzwerk Profils.</span><span class="sxs-lookup"><span data-stu-id="5259a-106">Contains the name of a network profile.</span></span> <span data-ttu-id="5259a-107">Der Name wird zu Anzeige Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="5259a-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="5259a-108">Das **Name** -Element wird durch den komplexen Typ [**networksettingstype**](taskschedulerschema-networksettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="5259a-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5259a-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5259a-109">Parent element</span></span>



| <span data-ttu-id="5259a-110">Element</span><span class="sxs-lookup"><span data-stu-id="5259a-110">Element</span></span>                                                                                            | <span data-ttu-id="5259a-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="5259a-111">Derived from</span></span>                                                                       | <span data-ttu-id="5259a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5259a-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5259a-113">**Network Settings (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="5259a-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="5259a-114">**Network settingstype**</span><span class="sxs-lookup"><span data-stu-id="5259a-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="5259a-115">Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5259a-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="5259a-116">Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5259a-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5259a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5259a-117">Remarks</span></span>

<span data-ttu-id="5259a-118">Informationen zur C++-Entwicklung finden Sie unter [**Name-Eigenschaft von inetworksettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="5259a-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="5259a-119">Informationen zur Skript Entwicklung finden Sie unter [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="5259a-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5259a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5259a-120">Requirements</span></span>



| <span data-ttu-id="5259a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5259a-121">Requirement</span></span> | <span data-ttu-id="5259a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5259a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5259a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5259a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5259a-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5259a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5259a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5259a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5259a-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5259a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





