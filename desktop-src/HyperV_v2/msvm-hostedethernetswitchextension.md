---
description: Ordnet den zurzeit an ihn gebundenen Erweiterungen einen virtuellen Ethernet-Switch zu.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Msvm_HostedEthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752384"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="6b851-103">MSVM- \_ Klasse "hustedethernetzwitchextension"</span><span class="sxs-lookup"><span data-stu-id="6b851-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="6b851-104">Ordnet den zurzeit an ihn gebundenen Erweiterungen einen virtuellen Ethernet-Switch zu.</span><span class="sxs-lookup"><span data-stu-id="6b851-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="6b851-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b851-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b851-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b851-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6b851-107">Member</span><span class="sxs-lookup"><span data-stu-id="6b851-107">Members</span></span>

<span data-ttu-id="6b851-108">Die **MSVM-Klasse " \_ hustedethernetzwitchextension** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b851-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="6b851-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b851-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b851-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b851-110">Properties</span></span>

<span data-ttu-id="6b851-111">Die **MSVM-Klasse " \_ hustedethernetzwitchextension** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b851-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b851-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6b851-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b851-113">Datentyp: **[ **MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="6b851-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6b851-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b851-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b851-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6b851-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6b851-116">Ein Verweis auf eine Instanz der [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) -Klasse, die den virtuellen Switch darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b851-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="6b851-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6b851-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b851-118">Datentyp: **[ **MSVM \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="6b851-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6b851-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b851-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b851-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b851-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b851-121">Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md) , die die switcherweiterungsinstanz darstellt, die an den virtuellen Switch gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="6b851-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b851-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b851-122">Requirements</span></span>



| <span data-ttu-id="6b851-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b851-123">Requirement</span></span> | <span data-ttu-id="6b851-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6b851-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b851-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b851-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b851-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b851-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b851-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b851-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b851-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b851-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b851-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b851-129">Namespace</span></span><br/>                | <span data-ttu-id="6b851-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6b851-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6b851-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6b851-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b851-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b851-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b851-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6b851-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b851-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b851-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

