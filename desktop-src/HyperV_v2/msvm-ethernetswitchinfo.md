---
description: Definiert die Zuordnung zwischen einem Ethernet-Switch und einer Switch-Ressource.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Msvm_EthernetSwitchInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961013"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="0669d-103">MSVM \_ ethernetzwitchinfo-Klasse</span><span class="sxs-lookup"><span data-stu-id="0669d-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="0669d-104">Definiert die Zuordnung zwischen einem Ethernet-Switch und einer Switch-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0669d-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="0669d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0669d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0669d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0669d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0669d-107">Member</span><span class="sxs-lookup"><span data-stu-id="0669d-107">Members</span></span>

<span data-ttu-id="0669d-108">Die **MSVM \_ ethernetzwitchinfo** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0669d-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="0669d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0669d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0669d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0669d-110">Properties</span></span>

<span data-ttu-id="0669d-111">Die **MSVM-Klasse " \_ ethernetzwitchinfo** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0669d-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0669d-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="0669d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0669d-113">Datentyp: **MSVM \_ virtualethernwitch**</span><span class="sxs-lookup"><span data-stu-id="0669d-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="0669d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0669d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0669d-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="0669d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0669d-116">Ein Verweis auf die Klasse " [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) ", die das Hostingsystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="0669d-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="0669d-117">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0669d-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="0669d-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="0669d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0669d-119">Datentyp: **MSVM \_ ethernetzwitchdata**</span><span class="sxs-lookup"><span data-stu-id="0669d-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="0669d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0669d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0669d-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="0669d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0669d-122">Ein Verweis auf die [**MSVM-Klasse " \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md) ", die die Switch-Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="0669d-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="0669d-123">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0669d-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0669d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0669d-124">Requirements</span></span>



| <span data-ttu-id="0669d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0669d-125">Requirement</span></span> | <span data-ttu-id="0669d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0669d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0669d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0669d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0669d-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0669d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0669d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0669d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0669d-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0669d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0669d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0669d-131">Namespace</span></span><br/>                | <span data-ttu-id="0669d-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0669d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0669d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0669d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0669d-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0669d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0669d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0669d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0669d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0669d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

