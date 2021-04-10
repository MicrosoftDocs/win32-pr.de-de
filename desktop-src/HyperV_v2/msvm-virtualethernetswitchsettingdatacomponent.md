---
description: Eine Zuordnung, die verwendet wird, um &\# 0034; Teil&\# 0034; Beziehungen zwischen einer Instanz von MSVM \_ virtualethernetzwitchsettingdata und einer oder mehreren Instanzen von MSVM \_ ethernettionwitchfeaturesettingdata herzustellen.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Msvm_VirtualEthernetSwitchSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215368"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="d1caf-103">MSVM \_ virtualethernetzwitchsettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1caf-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="d1caf-104">Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von [**MSVM \_ virtualethernettionwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) und einer oder mehreren Instanzen von [**MSVM \_ ethernettionwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d1caf-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="d1caf-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1caf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1caf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1caf-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d1caf-107">Member</span><span class="sxs-lookup"><span data-stu-id="d1caf-107">Members</span></span>

<span data-ttu-id="d1caf-108">Die **MSVM \_ virtualethernetzwitchsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d1caf-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d1caf-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1caf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1caf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1caf-110">Properties</span></span>

<span data-ttu-id="d1caf-111">Die **MSVM \_ virtualethernetzwitchsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1caf-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1caf-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d1caf-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-113">Datentyp: **MSVM \_ virtualethernetungwitchsettingdata**</span><span class="sxs-lookup"><span data-stu-id="d1caf-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1caf-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1caf-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-116">Verweis auf eine Instanz der [**MSVM \_ virtualethernetswitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) -Klasse, die einen Ethernet-Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1caf-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d1caf-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-118">Datentyp: **MSVM \_ ethernetzwitchfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="d1caf-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1caf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d1caf-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-121">Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) ", die die auf den Schalter angewendeten Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1caf-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1caf-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1caf-122">Requirements</span></span>



| <span data-ttu-id="d1caf-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1caf-123">Requirement</span></span> | <span data-ttu-id="d1caf-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d1caf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1caf-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1caf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1caf-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1caf-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1caf-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1caf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1caf-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1caf-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1caf-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1caf-129">Namespace</span></span><br/>                | <span data-ttu-id="d1caf-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1caf-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1caf-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d1caf-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1caf-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1caf-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1caf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d1caf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1caf-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1caf-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

