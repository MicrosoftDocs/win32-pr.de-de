---
description: Stellt eine generische Zuordnung dar, die verwendet wird, um Abhängigkeitsbeziehungen zwischen verwalteten Elementen herzustellen.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: CIM_Dependency-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345782"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="1f74f-103">CIM_Dependency-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="1f74f-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="1f74f-104">Stellt eine generische Zuordnung dar, die verwendet wird, um Abhängigkeitsbeziehungen zwischen verwalteten Elementen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1f74f-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f74f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f74f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1f74f-106">Member</span><span class="sxs-lookup"><span data-stu-id="1f74f-106">Members</span></span>

<span data-ttu-id="1f74f-107">Die **CIM- \_ Abhängigkeits** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1f74f-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="1f74f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f74f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f74f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f74f-109">Properties</span></span>

<span data-ttu-id="1f74f-110">Die **CIM- \_ Abhängigkeits** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f74f-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f74f-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="1f74f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f74f-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="1f74f-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1f74f-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f74f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f74f-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f74f-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f74f-115">Das unabhängige Objekt in dieser Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1f74f-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="1f74f-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="1f74f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f74f-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="1f74f-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1f74f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f74f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f74f-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f74f-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f74f-120">Das abhängige Objekt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1f74f-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f74f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f74f-121">Requirements</span></span>



| <span data-ttu-id="1f74f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f74f-122">Requirement</span></span> | <span data-ttu-id="1f74f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1f74f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f74f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f74f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f74f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1f74f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1f74f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f74f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f74f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f74f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1f74f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f74f-128">Namespace</span></span><br/>                | <span data-ttu-id="1f74f-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1f74f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1f74f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1f74f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f74f-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1f74f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f74f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f74f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f74f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f74f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

