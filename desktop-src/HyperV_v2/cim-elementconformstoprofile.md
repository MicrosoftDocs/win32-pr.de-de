---
description: Stellt eine Zuordnung dar, in der ein verwaltetes Element dem Standard eines registrierten Profils entspricht.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: CIM_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355527"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="73c9a-103">CIM \_ elementreformstoprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="73c9a-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="73c9a-104">Stellt eine Zuordnung dar, in der ein verwaltetes Element dem Standard eines registrierten Profils entspricht.</span><span class="sxs-lookup"><span data-stu-id="73c9a-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="73c9a-105">Diese Zuordnung gilt normalerweise für eine Instanz höherer Ebene, z. b. ein System, einen Namespace oder einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="73c9a-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="73c9a-106">Wenn Sie auf eine Instanz einer höheren Ebene angewendet werden, müssen sich alle Bestandteile entsprechend der Unterstützung der Übereinstimmung von managedelta für das benannte registeredprofile Verhalten.</span><span class="sxs-lookup"><span data-stu-id="73c9a-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c9a-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="73c9a-108">Member</span><span class="sxs-lookup"><span data-stu-id="73c9a-108">Members</span></span>

<span data-ttu-id="73c9a-109">Die **CIM \_ elementkonstoprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="73c9a-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="73c9a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73c9a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73c9a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73c9a-111">Properties</span></span>

<span data-ttu-id="73c9a-112">Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73c9a-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73c9a-113">**Conformantstandard**</span><span class="sxs-lookup"><span data-stu-id="73c9a-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c9a-114">Datentyp: **CIM \_ registeredprofile**</span><span class="sxs-lookup"><span data-stu-id="73c9a-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="73c9a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="73c9a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c9a-116">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73c9a-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73c9a-117">Das registrierte Profil, dem das verwaltete Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="73c9a-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="73c9a-118">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="73c9a-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c9a-119">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="73c9a-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="73c9a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="73c9a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c9a-121">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73c9a-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73c9a-122">Das verwaltete Element, das dem registrierten Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="73c9a-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73c9a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73c9a-123">Requirements</span></span>



| <span data-ttu-id="73c9a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73c9a-124">Requirement</span></span> | <span data-ttu-id="73c9a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="73c9a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c9a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73c9a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73c9a-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="73c9a-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="73c9a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73c9a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73c9a-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="73c9a-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="73c9a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="73c9a-130">Namespace</span></span><br/>                | <span data-ttu-id="73c9a-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="73c9a-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="73c9a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="73c9a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73c9a-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73c9a-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73c9a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="73c9a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73c9a-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73c9a-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

