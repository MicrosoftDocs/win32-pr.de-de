---
description: Stellt die Einstellungen für die Switch NIC-Team Vorgang dar.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Msvm_VirtualEthernetSwitchNicTeamingSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760849"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="3e67e-103">MSVM \_ virtualethernetzwitchnicteamingsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="3e67e-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="3e67e-104">Stellt die Einstellungen für die Switch NIC-Team Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="3e67e-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="3e67e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3e67e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e67e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e67e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="3e67e-107">Member</span><span class="sxs-lookup"><span data-stu-id="3e67e-107">Members</span></span>

<span data-ttu-id="3e67e-108">Die **MSVM \_ virtualethernetzwitchnicteamingsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3e67e-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3e67e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e67e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e67e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e67e-110">Properties</span></span>

<span data-ttu-id="3e67e-111">Die **MSVM \_ virtualethernetzwitchnicteamingsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3e67e-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e67e-112">**Loadbalancingalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="3e67e-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e67e-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e67e-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="3e67e-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3e67e-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3e67e-115">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3e67e-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3e67e-116">Der Lasten Ausgleichs Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="3e67e-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="3e67e-117">**Teamingmode**</span><span class="sxs-lookup"><span data-stu-id="3e67e-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e67e-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e67e-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="3e67e-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3e67e-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3e67e-120">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3e67e-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3e67e-121">Der Team Vorgangs Modus.</span><span class="sxs-lookup"><span data-stu-id="3e67e-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e67e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e67e-122">Requirements</span></span>



| <span data-ttu-id="3e67e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e67e-123">Requirement</span></span> | <span data-ttu-id="3e67e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3e67e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e67e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e67e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3e67e-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e67e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3e67e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e67e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3e67e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3e67e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3e67e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e67e-129">Namespace</span></span><br/>                | <span data-ttu-id="3e67e-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3e67e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e67e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3e67e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e67e-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3e67e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e67e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3e67e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e67e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e67e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e67e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e67e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e67e-136">**MSVM \_ ethernetzwitchfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="3e67e-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




