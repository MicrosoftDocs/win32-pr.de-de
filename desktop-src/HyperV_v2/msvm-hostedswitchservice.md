---
description: Eine Zuordnung, die einen virtuellen Switch-Dienst mit einem transparenten Überbrückungs Dienst verbindet.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346694"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="3a990-103">MSVM- \_ Klasse "hustedswitchservice"</span><span class="sxs-lookup"><span data-stu-id="3a990-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="3a990-104">Eine Zuordnung, die einen virtuellen Switch-Dienst mit einem transparenten Überbrückungs Dienst verbindet.</span><span class="sxs-lookup"><span data-stu-id="3a990-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="3a990-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a990-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a990-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a990-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3a990-107">Member</span><span class="sxs-lookup"><span data-stu-id="3a990-107">Members</span></span>

<span data-ttu-id="3a990-108">Die **MSVM-Klasse " \_ hustedswitchservice** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3a990-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="3a990-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a990-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a990-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a990-110">Properties</span></span>

<span data-ttu-id="3a990-111">Die **MSVM-Klasse " \_ hustedswitchservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a990-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a990-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3a990-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a990-113">Datentyp: **[ **MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="3a990-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3a990-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a990-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a990-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3a990-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3a990-116">Ein Verweis auf eine Instanz der [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) -Klasse, die den virtuellen Switch darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a990-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="3a990-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3a990-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a990-118">Datentyp: **[ **CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="3a990-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="3a990-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a990-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a990-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3a990-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3a990-121">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ transparentbridgingservice**](msvm-transparentbridgingservice.md) ", die den Überbrückungs Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a990-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a990-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a990-122">Remarks</span></span>

<span data-ttu-id="3a990-123">Der Zugriff auf die **MSVM-Klasse " \_ hustedswitchservice** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3a990-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3a990-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3a990-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a990-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a990-125">Requirements</span></span>



| <span data-ttu-id="3a990-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a990-126">Requirement</span></span> | <span data-ttu-id="3a990-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3a990-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a990-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a990-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a990-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a990-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a990-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a990-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a990-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a990-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a990-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a990-132">Namespace</span></span><br/>                | <span data-ttu-id="3a990-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a990-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a990-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3a990-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a990-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a990-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a990-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3a990-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a990-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a990-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a990-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a990-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a990-139">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="3a990-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="3a990-140">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="3a990-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

