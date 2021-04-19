---
description: Stellt eine Zuordnung zwischen einem Computersystem und der zuletzt angewendeten virtuellen System Momentaufnahme dar.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: CIM_LastAppliedSnapshot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355482"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="e0b4e-103">CIM \_ lastappliedsnapshot-Klasse</span><span class="sxs-lookup"><span data-stu-id="e0b4e-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="e0b4e-104">Stellt eine Zuordnung zwischen einem Computersystem und der zuletzt angewendeten virtuellen System Momentaufnahme dar.</span><span class="sxs-lookup"><span data-stu-id="e0b4e-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b4e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e0b4e-106">Member</span><span class="sxs-lookup"><span data-stu-id="e0b4e-106">Members</span></span>

<span data-ttu-id="e0b4e-107">Die **CIM- \_ lastappliedsnapshot** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e0b4e-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b4e-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b4e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b4e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b4e-109">Properties</span></span>

<span data-ttu-id="e0b4e-110">Die **CIM \_ lastappliedsnapshot** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0b4e-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b4e-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e0b4e-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b4e-112">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="e0b4e-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e0b4e-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b4e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b4e-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e0b4e-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e0b4e-115">Die Momentaufnahme des virtuellen Systems, die zuletzt auf das Computersystem angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e0b4e-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e0b4e-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e0b4e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b4e-117">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="e0b4e-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e0b4e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b4e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b4e-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e0b4e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e0b4e-120">Das Computersystem.</span><span class="sxs-lookup"><span data-stu-id="e0b4e-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0b4e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0b4e-121">Requirements</span></span>



| <span data-ttu-id="e0b4e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0b4e-122">Requirement</span></span> | <span data-ttu-id="e0b4e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e0b4e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b4e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0b4e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b4e-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e0b4e-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e0b4e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0b4e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b4e-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0b4e-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e0b4e-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0b4e-128">Namespace</span></span><br/>                | <span data-ttu-id="e0b4e-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0b4e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e0b4e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b4e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b4e-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e0b4e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b4e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b4e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b4e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0b4e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0b4e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0b4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b4e-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="e0b4e-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

