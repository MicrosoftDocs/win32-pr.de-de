---
description: Stellt die Daten der Routing Domänen Einstellung dar.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869271"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="9396d-103">MSVM \_ ethernetzwitchportroutingdomainsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="9396d-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="9396d-104">Stellt die Daten der Routing Domänen Einstellung dar.</span><span class="sxs-lookup"><span data-stu-id="9396d-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="9396d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9396d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9396d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9396d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="9396d-107">Member</span><span class="sxs-lookup"><span data-stu-id="9396d-107">Members</span></span>

<span data-ttu-id="9396d-108">Die **MSVM \_ ethernetzwitchportroutingdomainsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9396d-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9396d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9396d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9396d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9396d-110">Properties</span></span>

<span data-ttu-id="9396d-111">Die **MSVM \_ ethernetzwitchportroutingdomainsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9396d-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9396d-112">**Isolationidlist**</span><span class="sxs-lookup"><span data-stu-id="9396d-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9396d-113">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="9396d-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="9396d-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9396d-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9396d-115">Qualifizierer: **wmidataid** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9396d-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9396d-116">Die virtualsubnettid-oder VLAN-IDs für die Routing Domänen.</span><span class="sxs-lookup"><span data-stu-id="9396d-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="9396d-117">**Isolationidnamelist**</span><span class="sxs-lookup"><span data-stu-id="9396d-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9396d-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9396d-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9396d-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9396d-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9396d-120">Qualifizierer: **wmidataid** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9396d-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9396d-121">Das Array "virtualsubnettid" oder "VLAN-Anzeige Name".</span><span class="sxs-lookup"><span data-stu-id="9396d-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="9396d-122">**Routingdomainguid**</span><span class="sxs-lookup"><span data-stu-id="9396d-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9396d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9396d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9396d-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9396d-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9396d-125">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **wmidataid** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9396d-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9396d-126">Die GUID der Routing Domäne.</span><span class="sxs-lookup"><span data-stu-id="9396d-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9396d-127">**Routingdomainname**</span><span class="sxs-lookup"><span data-stu-id="9396d-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9396d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9396d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9396d-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9396d-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9396d-130">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9396d-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9396d-131">Der Anzeige Name der Routing Domäne.</span><span class="sxs-lookup"><span data-stu-id="9396d-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9396d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9396d-132">Requirements</span></span>



| <span data-ttu-id="9396d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9396d-133">Requirement</span></span> | <span data-ttu-id="9396d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9396d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9396d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9396d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9396d-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9396d-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9396d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9396d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9396d-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9396d-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9396d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9396d-139">Namespace</span></span><br/>                | <span data-ttu-id="9396d-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9396d-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9396d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9396d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9396d-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9396d-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9396d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9396d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9396d-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9396d-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9396d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9396d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9396d-146">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="9396d-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

