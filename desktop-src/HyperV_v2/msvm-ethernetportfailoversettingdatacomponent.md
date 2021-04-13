---
description: Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von MSVM \_ emuatedethernetportsettingdata und einer oder mehreren Instanzen eines MSVM- \_ ethernetzwitchfeaturesettingdata herzustellen.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529258"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="27407-103">MSVM \_ ethernetportfailoversettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="27407-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="27407-104">Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von [**MSVM \_ emuatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) und einer oder mehreren Instanzen eines [**MSVM- \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="27407-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="27407-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27407-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27407-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="27407-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="27407-107">Member</span><span class="sxs-lookup"><span data-stu-id="27407-107">Members</span></span>

<span data-ttu-id="27407-108">Die **MSVM-Klasse " \_ ethernetportfailoversettingdatacomponent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27407-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="27407-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27407-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27407-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27407-110">Properties</span></span>

<span data-ttu-id="27407-111">Die **MSVM-Klasse " \_ ethernetportfailoversettingdatacomponent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27407-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27407-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="27407-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27407-113">Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="27407-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="27407-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27407-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27407-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27407-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27407-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ emuatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) oder [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) , die den Ethernet-Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="27407-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="27407-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="27407-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27407-118">Datentyp: **[ **MSVM \_ failovernetworkadaptersettingdata**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="27407-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="27407-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27407-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27407-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="27407-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="27407-121">Ein Verweis auf eine Instanz der [**MSVM \_ failovernetworkadaptersettingdata**](msvm-failovernetworkadaptersettingdata.md) -Klasse, die die Konfiguration des Gastnetzwerk Adapters darstellt.</span><span class="sxs-lookup"><span data-stu-id="27407-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27407-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27407-122">Requirements</span></span>



| <span data-ttu-id="27407-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27407-123">Requirement</span></span> | <span data-ttu-id="27407-124">Wert</span><span class="sxs-lookup"><span data-stu-id="27407-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27407-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27407-125">Minimum supported client</span></span><br/> | <span data-ttu-id="27407-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27407-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="27407-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27407-127">Minimum supported server</span></span><br/> | <span data-ttu-id="27407-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27407-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27407-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="27407-129">Namespace</span></span><br/>                | <span data-ttu-id="27407-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="27407-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="27407-131">MOF</span><span class="sxs-lookup"><span data-stu-id="27407-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27407-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27407-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27407-133">DLL</span><span class="sxs-lookup"><span data-stu-id="27407-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27407-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27407-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

