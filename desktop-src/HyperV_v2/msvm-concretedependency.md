---
description: Definiert die Zuordnung zwischen einer installierten Ethernet-Switcherweiterung und einer Ethernet-Switcherweiterung.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Msvm_ConcreteDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215375"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="d4f7d-103">MSVM- \_ Klasse "concretedepend"</span><span class="sxs-lookup"><span data-stu-id="d4f7d-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="d4f7d-104">Definiert die Zuordnung zwischen einer installierten Ethernet-Switcherweiterung und einer Ethernet-Switcherweiterung.</span><span class="sxs-lookup"><span data-stu-id="d4f7d-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="d4f7d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4f7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4f7d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d4f7d-107">Member</span><span class="sxs-lookup"><span data-stu-id="d4f7d-107">Members</span></span>

<span data-ttu-id="d4f7d-108">Die **MSVM-Klasse " \_ concretedepend** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4f7d-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d4f7d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4f7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4f7d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4f7d-110">Properties</span></span>

<span data-ttu-id="d4f7d-111">Die **MSVM-Klasse " \_ concretedepend** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4f7d-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4f7d-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d4f7d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4f7d-113">Datentyp: **[ **MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="d4f7d-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="d4f7d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4f7d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4f7d-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="d4f7d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d4f7d-116">Ein Verweis auf eine Instanz der [**MSVM \_ installedethernetswitchextension**](msvm-installedethernetswitchextension.md) -Klasse, die eine Komponente für eine virtuelle Ethernet-Switcherweiterung darstellt, die auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d4f7d-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4f7d-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d4f7d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4f7d-118">Datentyp: **[ **MSVM \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="d4f7d-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="d4f7d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4f7d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4f7d-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="d4f7d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d4f7d-121">Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ ethernetswitchextension**](msvm-ethernetswitchextension.md) , die das Vorkommen des Vorgängers darstellt, der an einen bestimmten virtuellen Ethernet- **Switch gebunden ist** .</span><span class="sxs-lookup"><span data-stu-id="d4f7d-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4f7d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4f7d-122">Requirements</span></span>



| <span data-ttu-id="d4f7d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4f7d-123">Requirement</span></span> | <span data-ttu-id="d4f7d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d4f7d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f7d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4f7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f7d-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4f7d-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4f7d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4f7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f7d-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4f7d-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4f7d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4f7d-129">Namespace</span></span><br/>                | <span data-ttu-id="d4f7d-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d4f7d-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4f7d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d4f7d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4f7d-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4f7d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f7d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f7d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

