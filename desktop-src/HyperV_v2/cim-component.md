---
description: Stellt eine generische Zuordnung zwischen einem übergeordneten verwalteten Element und einem untergeordneten verwalteten Element dar, bei dem das untergeordnete Element eine Komponente oder einen Teil des übergeordneten Elements darstellt.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: CIM_Component-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359113"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="5fa15-103">CIM_Component-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="5fa15-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="5fa15-104">Stellt eine generische Zuordnung zwischen einem übergeordneten verwalteten Element und einem untergeordneten verwalteten Element dar, bei dem das untergeordnete Element eine Komponente oder einen Teil des übergeordneten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fa15-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fa15-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="5fa15-106">Member</span><span class="sxs-lookup"><span data-stu-id="5fa15-106">Members</span></span>

<span data-ttu-id="5fa15-107">Die **CIM- \_ Komponenten** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5fa15-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="5fa15-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fa15-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fa15-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fa15-109">Properties</span></span>

<span data-ttu-id="5fa15-110">Die **CIM- \_ Komponenten** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5fa15-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fa15-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5fa15-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa15-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="5fa15-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5fa15-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa15-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa15-114">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5fa15-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5fa15-115">Das übergeordnete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="5fa15-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="5fa15-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5fa15-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa15-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="5fa15-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5fa15-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa15-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa15-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fa15-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fa15-120">Das untergeordnete-Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="5fa15-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fa15-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fa15-121">Requirements</span></span>



| <span data-ttu-id="5fa15-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fa15-122">Requirement</span></span> | <span data-ttu-id="5fa15-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5fa15-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa15-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fa15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa15-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5fa15-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5fa15-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fa15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa15-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fa15-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5fa15-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fa15-128">Namespace</span></span><br/>                | <span data-ttu-id="5fa15-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5fa15-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5fa15-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5fa15-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fa15-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5fa15-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fa15-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa15-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fa15-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fa15-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

