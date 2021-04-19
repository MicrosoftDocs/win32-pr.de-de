---
description: Stellt eine Zuordnung dar, in der ein Bridge Dienst eine Komponente eines Switch-Dienstanbieter ist.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: CIM_SwitchServiceTransparentBridging-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349778"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="95f6a-103">CIM \_ switchservicetransparentbridging-Klasse</span><span class="sxs-lookup"><span data-stu-id="95f6a-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="95f6a-104">Stellt eine Zuordnung dar, in der ein Bridge Dienst eine Komponente eines Switch-Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="95f6a-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f6a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f6a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="95f6a-106">Member</span><span class="sxs-lookup"><span data-stu-id="95f6a-106">Members</span></span>

<span data-ttu-id="95f6a-107">Die **CIM \_ switchservicetransparentbridging** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="95f6a-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="95f6a-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95f6a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95f6a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95f6a-109">Properties</span></span>

<span data-ttu-id="95f6a-110">Die **CIM \_ switchservicetransparentbridging** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95f6a-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95f6a-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="95f6a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f6a-112">Datentyp: **CIM \_ switchservice**</span><span class="sxs-lookup"><span data-stu-id="95f6a-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="95f6a-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f6a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f6a-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="95f6a-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="95f6a-115">Ein [**CIM \_ switchservice**](cim-switchservice.md) -Verweis auf den Switch-Dienst.</span><span class="sxs-lookup"><span data-stu-id="95f6a-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="95f6a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="95f6a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f6a-117">Datentyp: **CIM \_ transparentbridgingservice**</span><span class="sxs-lookup"><span data-stu-id="95f6a-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="95f6a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95f6a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f6a-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="95f6a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="95f6a-120">Ein [**CIM- \_ transparentbridgingservice**](cim-transparentbridgingservice.md) -Verweis auf den Komponenten Überbrückungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="95f6a-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95f6a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95f6a-121">Requirements</span></span>



| <span data-ttu-id="95f6a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95f6a-122">Requirement</span></span> | <span data-ttu-id="95f6a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="95f6a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f6a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95f6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95f6a-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95f6a-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="95f6a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95f6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95f6a-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="95f6a-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="95f6a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="95f6a-128">Namespace</span></span><br/>                | <span data-ttu-id="95f6a-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="95f6a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95f6a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="95f6a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f6a-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95f6a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95f6a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95f6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f6a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95f6a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95f6a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95f6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f6a-135">**CIM- \_ ServiceComponent**</span><span class="sxs-lookup"><span data-stu-id="95f6a-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

