---
description: Stellt die Zuordnung zwischen einem Team externalethernetport und einem externalethernetport-Member dar.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Msvm_VirtualEthernetSwitchNicTeamingMember-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218856"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="2a4f3-103">MSVM \_ virtualethernetzwitchnicteamingmember-Klasse</span><span class="sxs-lookup"><span data-stu-id="2a4f3-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="2a4f3-104">Stellt die Zuordnung zwischen einem Team externalethernetport und einem externalethernetport-Member dar.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="2a4f3-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4f3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a4f3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2a4f3-107">Member</span><span class="sxs-lookup"><span data-stu-id="2a4f3-107">Members</span></span>

<span data-ttu-id="2a4f3-108">Die **MSVM \_ virtualethernettwitchnicteamingmember** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a4f3-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="2a4f3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a4f3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a4f3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a4f3-110">Properties</span></span>

<span data-ttu-id="2a4f3-111">Die **MSVM \_ virtualethernetzwitchnicteamingmember** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a4f3-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4f3-113">Datentyp: **MSVM \_ externalethernetport**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="2a4f3-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a4f3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4f3-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="2a4f3-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2a4f3-116">Eine [**MSVM \_ externalethernetport**](msvm-externalethernetport.md) , die auf die Instanz des externen Ethernet-Ports verweist.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="2a4f3-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4f3-118">Datentyp: **MSVM \_ externalethernetport**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="2a4f3-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a4f3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4f3-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="2a4f3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2a4f3-121">Verweis auf die [**MSVM \_ externalethernetport**](msvm-externalethernetport.md) -Mitglieder Instanz.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a4f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a4f3-122">Requirements</span></span>



| <span data-ttu-id="2a4f3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a4f3-123">Requirement</span></span> | <span data-ttu-id="2a4f3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2a4f3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4f3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a4f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2a4f3-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a4f3-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2a4f3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a4f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2a4f3-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2a4f3-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2a4f3-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a4f3-129">Namespace</span></span><br/>                | <span data-ttu-id="2a4f3-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a4f3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2a4f3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2a4f3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a4f3-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a4f3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4f3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a4f3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a4f3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a4f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4f3-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

