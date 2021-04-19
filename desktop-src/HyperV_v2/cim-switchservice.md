---
description: Stellt einen switchdienst dar.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: CIM_SwitchService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372984"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="b80bc-103">CIM \_ switchservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b80bc-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="b80bc-104">Stellt einen switchdienst dar.</span><span class="sxs-lookup"><span data-stu-id="b80bc-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b80bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b80bc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="b80bc-106">Member</span><span class="sxs-lookup"><span data-stu-id="b80bc-106">Members</span></span>

<span data-ttu-id="b80bc-107">Die **CIM \_ switchservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b80bc-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="b80bc-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b80bc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b80bc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b80bc-109">Properties</span></span>

<span data-ttu-id="b80bc-110">Die **CIM \_ switchservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b80bc-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b80bc-111">**Bridgeaddress**</span><span class="sxs-lookup"><span data-stu-id="b80bc-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b80bc-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b80bc-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b80bc-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-114">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ switchservice**".**Bridgeadresssstype**")</span><span class="sxs-lookup"><span data-stu-id="b80bc-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="b80bc-115">Die Adresse des Switch-Dienstanbieter, der Teil des eindeutigen Bezeichners des Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="b80bc-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="b80bc-116">**Bridgeadresssstype**</span><span class="sxs-lookup"><span data-stu-id="b80bc-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b80bc-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b80bc-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b80bc-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-119">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ switchservice**".**Bridgeaddress**")</span><span class="sxs-lookup"><span data-stu-id="b80bc-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="b80bc-120">Das Adressierungs Format, das für die Bridge und die **bridgeaddress** -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b80bc-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b80bc-121">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b80bc-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="b80bc-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="b80bc-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="b80bc-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="b80bc-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="b80bc-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="b80bc-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="b80bc-125">**Mac +** Aufteilungs Struktur Priorität (5)</span><span class="sxs-lookup"><span data-stu-id="b80bc-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b80bc-126">**Bridgetype**</span><span class="sxs-lookup"><span data-stu-id="b80bc-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b80bc-127">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b80bc-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b80bc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="b80bc-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="b80bc-130">Der Typ des auszuführenden Wechsel Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b80bc-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b80bc-131">**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="b80bc-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="b80bc-132">**Nur transparent** (2)</span><span class="sxs-lookup"><span data-stu-id="b80bc-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="b80bc-133">**Nur SourceRoute** (3)</span><span class="sxs-lookup"><span data-stu-id="b80bc-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="b80bc-134">**SRT** (4)</span><span class="sxs-lookup"><span data-stu-id="b80bc-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b80bc-135">**Numports**</span><span class="sxs-lookup"><span data-stu-id="b80bc-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b80bc-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b80bc-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b80bc-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b80bc-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="b80bc-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="b80bc-139">Die Anzahl der Switchports, die von diesem Wechseldienst gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="b80bc-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b80bc-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b80bc-140">Requirements</span></span>



| <span data-ttu-id="b80bc-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b80bc-141">Requirement</span></span> | <span data-ttu-id="b80bc-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b80bc-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b80bc-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b80bc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b80bc-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b80bc-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b80bc-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b80bc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b80bc-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b80bc-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b80bc-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b80bc-147">Namespace</span></span><br/>                | <span data-ttu-id="b80bc-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b80bc-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b80bc-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b80bc-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b80bc-150"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b80bc-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b80bc-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b80bc-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b80bc-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b80bc-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b80bc-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b80bc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b80bc-154">**CIM- \_ weiterforwardingdienst**</span><span class="sxs-lookup"><span data-stu-id="b80bc-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

