---
title: ID-Element (networksettingstype)
description: Enthält einen GUID-Wert, der ein Netzwerk Profil identifiziert.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- ID-Element Taskplaner
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106370"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="9494d-104">ID-Element (networksettingstype)</span><span class="sxs-lookup"><span data-stu-id="9494d-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="9494d-105">Enthält einen GUID-Wert, der ein Netzwerk Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9494d-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="9494d-106">Das **ID** -Element wird durch den komplexen Typ [**networksettingstype**](taskschedulerschema-networksettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="9494d-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9494d-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="9494d-107">Parent element</span></span>



| <span data-ttu-id="9494d-108">Element</span><span class="sxs-lookup"><span data-stu-id="9494d-108">Element</span></span>                                                                                            | <span data-ttu-id="9494d-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="9494d-109">Derived from</span></span>                                                                       | <span data-ttu-id="9494d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9494d-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9494d-111">**Network Settings (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="9494d-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="9494d-112">**Network settingstype**</span><span class="sxs-lookup"><span data-stu-id="9494d-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="9494d-113">Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9494d-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="9494d-114">Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9494d-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9494d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9494d-115">Remarks</span></span>

<span data-ttu-id="9494d-116">Informationen zur C++-Entwicklung finden Sie unter [**ID-Eigenschaft von inetworksettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="9494d-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="9494d-117">Informationen zur Skript Entwicklung finden Sie unter [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="9494d-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9494d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9494d-118">Requirements</span></span>



| <span data-ttu-id="9494d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9494d-119">Requirement</span></span> | <span data-ttu-id="9494d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9494d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9494d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9494d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9494d-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9494d-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9494d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9494d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9494d-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9494d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





