---
description: Stellt die Zuordnung zwischen einer übergeordneten Ethernet-Switcherweiterung und einer untergeordneten Ethernet-Switcherweiterung dar.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Msvm_ParentEthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363754"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="e463f-103">MSVM- \_ Parametererweiterung-Klasse</span><span class="sxs-lookup"><span data-stu-id="e463f-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="e463f-104">Stellt die Zuordnung zwischen einer übergeordneten Ethernet-Switcherweiterung und einer untergeordneten Ethernet-Switcherweiterung dar.</span><span class="sxs-lookup"><span data-stu-id="e463f-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="e463f-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e463f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e463f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e463f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e463f-107">Member</span><span class="sxs-lookup"><span data-stu-id="e463f-107">Members</span></span>

<span data-ttu-id="e463f-108">Die **MSVM \_** -Klasse "Parser-Erweiterung" verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e463f-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="e463f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e463f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e463f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e463f-110">Properties</span></span>

<span data-ttu-id="e463f-111">Die **MSVM \_** -Klasse "Parser-Erweiterung" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e463f-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e463f-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e463f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e463f-113">Datentyp: **[ **MSVM \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="e463f-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e463f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e463f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e463f-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="e463f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e463f-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchextension**](msvm-ethernetswitchextension.md) ", die die übergeordnete Switcherweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e463f-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="e463f-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e463f-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e463f-118">Datentyp: **[ **MSVM \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="e463f-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e463f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e463f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e463f-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="e463f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e463f-121">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchextension**](msvm-ethernetswitchextension.md) ", die die untergeordnete Switcherweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e463f-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e463f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e463f-122">Requirements</span></span>



| <span data-ttu-id="e463f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e463f-123">Requirement</span></span> | <span data-ttu-id="e463f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e463f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e463f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e463f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e463f-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e463f-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e463f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e463f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e463f-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e463f-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e463f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e463f-129">Namespace</span></span><br/>                | <span data-ttu-id="e463f-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e463f-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e463f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e463f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e463f-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e463f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e463f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e463f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e463f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e463f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

