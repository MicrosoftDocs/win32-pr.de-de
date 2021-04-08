---
description: Stellt eine Zuordnung zwischen einem System und einem der Elemente dar, die es bilden.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: CIM_SystemComponent-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864119"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="aa1b0-103">CIM_SystemComponent-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="aa1b0-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="aa1b0-104">Stellt eine Zuordnung zwischen einem System und einem der Elemente dar, die es bilden.</span><span class="sxs-lookup"><span data-stu-id="aa1b0-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa1b0-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="aa1b0-106">Member</span><span class="sxs-lookup"><span data-stu-id="aa1b0-106">Members</span></span>

<span data-ttu-id="aa1b0-107">Die **CIM \_ SystemComponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa1b0-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="aa1b0-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa1b0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa1b0-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa1b0-109">Properties</span></span>

<span data-ttu-id="aa1b0-110">Die **CIM \_ SystemComponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa1b0-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa1b0-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="aa1b0-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa1b0-112">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="aa1b0-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="aa1b0-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa1b0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa1b0-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="aa1b0-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aa1b0-115">Das [**CIM- \_ System**](cim-system.md) , das die **PartComponent** enthält.</span><span class="sxs-lookup"><span data-stu-id="aa1b0-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="aa1b0-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="aa1b0-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa1b0-117">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="aa1b0-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="aa1b0-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa1b0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa1b0-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="aa1b0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aa1b0-120">Das untergeordnete [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das eine Komponente des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="aa1b0-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa1b0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa1b0-121">Requirements</span></span>



| <span data-ttu-id="aa1b0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa1b0-122">Requirement</span></span> | <span data-ttu-id="aa1b0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="aa1b0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1b0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa1b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1b0-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa1b0-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="aa1b0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa1b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1b0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa1b0-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="aa1b0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa1b0-128">Namespace</span></span><br/>                | <span data-ttu-id="aa1b0-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa1b0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa1b0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="aa1b0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa1b0-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa1b0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa1b0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aa1b0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa1b0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa1b0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa1b0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa1b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1b0-135">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="aa1b0-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

