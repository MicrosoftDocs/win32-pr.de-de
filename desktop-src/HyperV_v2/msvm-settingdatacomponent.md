---
description: Richten Sie eine Beziehung zwischen einer Instanz der MSVM- \_ emulatedethernetportsettingdata-Klasse oder der MSVM \_ syntheticethernetportsettingdata-Klasse mit einer Instanz der MSVM \_ guestnetworkadapterconfiguration-Klasse ein.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960070"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="73f61-103">MSVM \_ settingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="73f61-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="73f61-104">Richten Sie eine Beziehung zwischen einer Instanz der [**MSVM- \_ emulatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) -Klasse oder der [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) -Klasse mit einer Instanz der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse ein.</span><span class="sxs-lookup"><span data-stu-id="73f61-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="73f61-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73f61-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f61-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73f61-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="73f61-107">Member</span><span class="sxs-lookup"><span data-stu-id="73f61-107">Members</span></span>

<span data-ttu-id="73f61-108">Die **MSVM \_ settingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="73f61-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="73f61-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73f61-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73f61-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73f61-110">Properties</span></span>

<span data-ttu-id="73f61-111">Die **MSVM \_ settingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73f61-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73f61-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="73f61-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f61-113">Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="73f61-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="73f61-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="73f61-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f61-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="73f61-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="73f61-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ emuatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) oder [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) , die einen Ethernet-Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="73f61-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="73f61-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="73f61-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f61-118">Datentyp: **[ **MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="73f61-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="73f61-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="73f61-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f61-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="73f61-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="73f61-121">Ein Verweis auf eine Instanz der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse, die die Konfiguration eines Gastnetzwerk Adapters darstellt.</span><span class="sxs-lookup"><span data-stu-id="73f61-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73f61-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73f61-122">Requirements</span></span>



| <span data-ttu-id="73f61-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73f61-123">Requirement</span></span> | <span data-ttu-id="73f61-124">Wert</span><span class="sxs-lookup"><span data-stu-id="73f61-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f61-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73f61-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73f61-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73f61-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="73f61-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73f61-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73f61-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73f61-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73f61-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="73f61-129">Namespace</span></span><br/>                | <span data-ttu-id="73f61-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="73f61-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="73f61-131">MOF</span><span class="sxs-lookup"><span data-stu-id="73f61-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73f61-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73f61-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73f61-133">DLL</span><span class="sxs-lookup"><span data-stu-id="73f61-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f61-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73f61-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

