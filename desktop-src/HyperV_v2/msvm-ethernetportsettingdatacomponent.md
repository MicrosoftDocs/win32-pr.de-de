---
description: Eine Zuordnung, die verwendet wird, um &\# 0034; Teil&\# 0034; Beziehungen zwischen einer Instanz von MSVM \_ ethernetportzuordcationsettingdata und einer oder mehreren Instanzen von MSVM \_ ethernettionwitchfeaturesettingdata herzustellen.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347612"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="96017-103">MSVM \_ ethernetportsettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="96017-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="96017-104">Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz eines [**MSVM- \_ ethernetportzuordnungsdateils**](msvm-ethernetportallocationsettingdata.md) und einer oder mehreren Instanzen eines [**MSVM- \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96017-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="96017-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96017-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96017-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="96017-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="96017-107">Member</span><span class="sxs-lookup"><span data-stu-id="96017-107">Members</span></span>

<span data-ttu-id="96017-108">Die **MSVM-Klasse " \_ ethernetportsettingdatacomponent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="96017-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="96017-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96017-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96017-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96017-110">Properties</span></span>

<span data-ttu-id="96017-111">Die **MSVM-Klasse " \_ ethernetportsettingdatacomponent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96017-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96017-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="96017-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96017-113">Datentyp: **[ **MSVM \_ ethernetportzugecationsettingdata**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="96017-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="96017-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96017-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96017-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="96017-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="96017-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetportzuweisung**](msvm-ethernetportallocationsettingdata.md) ", die den Ethernet-Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="96017-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="96017-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="96017-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96017-118">Datentyp: **[ **MSVM \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="96017-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="96017-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="96017-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96017-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="96017-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="96017-121">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md) ", die die auf den Port angewendeten Funktionseinstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="96017-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96017-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96017-122">Requirements</span></span>



| <span data-ttu-id="96017-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96017-123">Requirement</span></span> | <span data-ttu-id="96017-124">Wert</span><span class="sxs-lookup"><span data-stu-id="96017-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96017-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96017-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96017-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96017-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="96017-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96017-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96017-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96017-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96017-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="96017-129">Namespace</span></span><br/>                | <span data-ttu-id="96017-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="96017-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="96017-131">MOF</span><span class="sxs-lookup"><span data-stu-id="96017-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96017-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="96017-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96017-133">DLL</span><span class="sxs-lookup"><span data-stu-id="96017-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96017-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96017-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

