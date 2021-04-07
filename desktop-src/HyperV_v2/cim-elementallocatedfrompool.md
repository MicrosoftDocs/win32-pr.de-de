---
description: Stellt eine Zuordnung dar, in der ein CIM \_ LogicalElement-Objekt eine Ressource darstellt, die von einem CIM- \_ resourcepool-Objekt zugeordnet wird.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: CIM_ElementAllocatedFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863116"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="5931d-103">CIM- \_ elementzudepedfrompool-Klasse</span><span class="sxs-lookup"><span data-stu-id="5931d-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="5931d-104">Stellt eine Zuordnung dar, in der ein [**CIM \_ LogicalElement**](cim-logicalelement.md) -Objekt eine Ressource darstellt, die von einem [**CIM- \_ resourcepool**](cim-resourcepool.md) -Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5931d-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5931d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5931d-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5931d-106">Member</span><span class="sxs-lookup"><span data-stu-id="5931d-106">Members</span></span>

<span data-ttu-id="5931d-107">Die **CIM- \_ elementzudepedfrompool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5931d-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="5931d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5931d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5931d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5931d-109">Properties</span></span>

<span data-ttu-id="5931d-110">Die **CIM \_ elementzuzuedfrompool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5931d-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5931d-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5931d-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5931d-112">Datentyp: **CIM \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="5931d-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="5931d-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5931d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5931d-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="5931d-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5931d-115">Der Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="5931d-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="5931d-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5931d-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5931d-117">Datentyp: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5931d-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="5931d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5931d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5931d-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="5931d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5931d-120">Die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="5931d-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5931d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5931d-121">Requirements</span></span>



| <span data-ttu-id="5931d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5931d-122">Requirement</span></span> | <span data-ttu-id="5931d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5931d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5931d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5931d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5931d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5931d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5931d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5931d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5931d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5931d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5931d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5931d-128">Namespace</span></span><br/>                | <span data-ttu-id="5931d-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5931d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5931d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5931d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5931d-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5931d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5931d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5931d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5931d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5931d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5931d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5931d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5931d-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="5931d-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

