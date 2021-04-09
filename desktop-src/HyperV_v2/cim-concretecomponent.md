---
description: Stellt eine generische Zuordnung dar, die verwendet wird, um die Teile einer Beziehung zwischen verwalteten Elementen herzustellen.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: CIM_ConcreteComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865783"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="80045-103">CIM- \_ Klasse "concretecomponent"</span><span class="sxs-lookup"><span data-stu-id="80045-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="80045-104">Stellt eine generische Zuordnung dar, die verwendet wird, um die Teile einer Beziehung zwischen verwalteten Elementen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="80045-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="80045-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80045-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="80045-106">Member</span><span class="sxs-lookup"><span data-stu-id="80045-106">Members</span></span>

<span data-ttu-id="80045-107">Die CIM-Klasse " **\_ concretecomponent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="80045-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="80045-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80045-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80045-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80045-109">Properties</span></span>

<span data-ttu-id="80045-110">Die CIM-Klasse " **\_ concretecomponent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80045-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80045-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="80045-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80045-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="80045-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="80045-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80045-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80045-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="80045-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="80045-115">Das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="80045-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="80045-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="80045-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80045-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="80045-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="80045-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80045-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80045-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="80045-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="80045-120">Das untergeordnete-Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="80045-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80045-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80045-121">Requirements</span></span>



| <span data-ttu-id="80045-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80045-122">Requirement</span></span> | <span data-ttu-id="80045-123">Wert</span><span class="sxs-lookup"><span data-stu-id="80045-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80045-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80045-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80045-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="80045-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="80045-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80045-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80045-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80045-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="80045-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="80045-128">Namespace</span></span><br/>                | <span data-ttu-id="80045-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="80045-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80045-130">MOF</span><span class="sxs-lookup"><span data-stu-id="80045-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80045-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="80045-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80045-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80045-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80045-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80045-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80045-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80045-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80045-135">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="80045-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

