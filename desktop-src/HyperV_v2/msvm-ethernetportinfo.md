---
description: Eine Zuordnung zwischen einer Instanz der MSVM \_ ethernetungwitchport-Klasse und einer Instanz der MSVM- \_ Klasse "ethernetportdata", die die Daten darstellt, die über den Port durch eine Switcherweiterung gesammelt werden.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353506"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="935ba-103">MSVM- \_ Klasse "ethernetportinfo"</span><span class="sxs-lookup"><span data-stu-id="935ba-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="935ba-104">Eine Zuordnung zwischen einer Instanz der [**MSVM \_ ethernetungwitchport**](msvm-ethernetswitchport.md) -Klasse und einer Instanz der [**MSVM-Klasse " \_ ethernetportdata**](msvm-ethernetportdata.md) ", die die Daten darstellt, die über den Port durch eine Switcherweiterung gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="935ba-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="935ba-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="935ba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="935ba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="935ba-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="935ba-107">Member</span><span class="sxs-lookup"><span data-stu-id="935ba-107">Members</span></span>

<span data-ttu-id="935ba-108">Die **MSVM-Klasse " \_ ethernetportinfo** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="935ba-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="935ba-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="935ba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="935ba-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="935ba-110">Properties</span></span>

<span data-ttu-id="935ba-111">Die **MSVM-Klasse " \_ ethernetportinfo** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="935ba-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="935ba-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="935ba-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935ba-113">Datentyp: **MSVM \_ ethernetzwitchport**</span><span class="sxs-lookup"><span data-stu-id="935ba-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="935ba-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935ba-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935ba-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="935ba-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="935ba-116">Eine Instanz der [**MSVM \_ ethernetzwitchport**](msvm-ethernetswitchport.md) -Klasse, die den Switchport darstellt.</span><span class="sxs-lookup"><span data-stu-id="935ba-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="935ba-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="935ba-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935ba-118">Datentyp: **MSVM \_ ethernetportdata**</span><span class="sxs-lookup"><span data-stu-id="935ba-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="935ba-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935ba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935ba-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="935ba-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="935ba-121">Eine Instanz der [**MSVM-Klasse " \_ ethernetportdata**](msvm-ethernetportdata.md) ", die die Portdaten darstellt.</span><span class="sxs-lookup"><span data-stu-id="935ba-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="935ba-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="935ba-122">Requirements</span></span>



| <span data-ttu-id="935ba-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="935ba-123">Requirement</span></span> | <span data-ttu-id="935ba-124">Wert</span><span class="sxs-lookup"><span data-stu-id="935ba-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935ba-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="935ba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="935ba-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="935ba-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="935ba-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="935ba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="935ba-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="935ba-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="935ba-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="935ba-129">Namespace</span></span><br/>                | <span data-ttu-id="935ba-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="935ba-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="935ba-131">MOF</span><span class="sxs-lookup"><span data-stu-id="935ba-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="935ba-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="935ba-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="935ba-133">DLL</span><span class="sxs-lookup"><span data-stu-id="935ba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="935ba-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="935ba-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

