---
description: Stellt den transparenten Überbrückungs Aspekt eines CIM \_ switchservice-Objekts dar.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864112"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="2c728-103">CIM- \_ transparentbridgingservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c728-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="2c728-104">Stellt den transparenten Überbrückungs Aspekt eines [**CIM \_ switchservice**](cim-switchservice.md) -Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="2c728-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c728-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c728-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="2c728-106">Member</span><span class="sxs-lookup"><span data-stu-id="2c728-106">Members</span></span>

<span data-ttu-id="2c728-107">Die CIM-Klasse " **\_ transparentbridgingservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c728-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="2c728-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c728-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c728-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c728-109">Properties</span></span>

<span data-ttu-id="2c728-110">Die CIM-Klasse " **\_ transparentbridgingservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c728-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c728-111">**Agingtime**</span><span class="sxs-lookup"><span data-stu-id="2c728-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c728-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c728-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c728-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c728-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c728-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="2c728-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="2c728-115">Der Timeout Zeitraum (in Sekunden) für das Auslagern dynamisch erlernter Weiterleitungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c728-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="2c728-116">Der 802.1 d-1990-Standard empfiehlt einen Standardwert von 300 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2c728-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2c728-117">**Angestrebt**</span><span class="sxs-lookup"><span data-stu-id="2c728-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c728-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c728-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c728-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c728-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c728-120">Filtern von Daten Bank Bezeichnern, die von VLAN-fähigen Switches verwendet werden, die über mehrere Filter Datenbanken verfügen.</span><span class="sxs-lookup"><span data-stu-id="2c728-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c728-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c728-121">Requirements</span></span>



| <span data-ttu-id="2c728-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c728-122">Requirement</span></span> | <span data-ttu-id="2c728-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2c728-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c728-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c728-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c728-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c728-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2c728-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c728-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c728-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c728-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2c728-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c728-128">Namespace</span></span><br/>                | <span data-ttu-id="2c728-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c728-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c728-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2c728-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c728-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c728-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c728-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c728-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c728-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c728-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c728-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c728-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c728-135">**CIM- \_ weiterforwardingdienst**</span><span class="sxs-lookup"><span data-stu-id="2c728-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

