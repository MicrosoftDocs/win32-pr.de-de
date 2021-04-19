---
description: Definiert die registrierten Profile, denen das referenzierte System entspricht.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363592"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="7bce9-103">MSVM \_ elementreformstoprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="7bce9-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="7bce9-104">Definiert die registrierten Profile, denen das referenzierte System entspricht.</span><span class="sxs-lookup"><span data-stu-id="7bce9-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="7bce9-105">Diese Zuordnung kann auf ein beliebiges verwaltetes Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bce9-105">This association may apply to any managed element.</span></span> <span data-ttu-id="7bce9-106">Die typische Verwendung wird auf eine Instanz höherer Ebene angewendet, z. b. auf ein System, einen Namespace oder einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="7bce9-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="7bce9-107">Wenn Sie auf eine Instanz einer höheren Ebene angewendet werden, müssen sich alle Bestandteile entsprechend der Unterstützung der Übereinstimmung des verwalteten Elements mit dem benannten registrierten Profil Verhalten.</span><span class="sxs-lookup"><span data-stu-id="7bce9-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="7bce9-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7bce9-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bce9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bce9-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="7bce9-110">Member</span><span class="sxs-lookup"><span data-stu-id="7bce9-110">Members</span></span>

<span data-ttu-id="7bce9-111">Die **MSVM \_ elementkonformstoprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7bce9-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="7bce9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7bce9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bce9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7bce9-113">Properties</span></span>

<span data-ttu-id="7bce9-114">Die **MSVM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7bce9-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bce9-115">**Conformantstandard**</span><span class="sxs-lookup"><span data-stu-id="7bce9-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce9-116">Datentyp: **[ **MSVM \_ registeredprofile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="7bce9-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7bce9-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7bce9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bce9-118">Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bce9-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bce9-119">Ein Verweis auf eine Instanz der [**MSVM \_ registeredprofile**](msvm-registeredprofile.md) -Klasse, die das registrierte Profil darstellt, dem das System entspricht.</span><span class="sxs-lookup"><span data-stu-id="7bce9-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="7bce9-120">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="7bce9-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce9-121">Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="7bce9-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7bce9-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7bce9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bce9-123">Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bce9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bce9-124">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das System darstellt, das dem registrierten Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="7bce9-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bce9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bce9-125">Requirements</span></span>



| <span data-ttu-id="7bce9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bce9-126">Requirement</span></span> | <span data-ttu-id="7bce9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7bce9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bce9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bce9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7bce9-129">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7bce9-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7bce9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bce9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7bce9-131">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bce9-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7bce9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bce9-132">Namespace</span></span><br/>                | <span data-ttu-id="7bce9-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7bce9-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7bce9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7bce9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bce9-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7bce9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bce9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7bce9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bce9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7bce9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

