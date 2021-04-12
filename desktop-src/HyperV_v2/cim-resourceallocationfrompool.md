---
description: Stellt eine Zuordnung dar, in der eine CIM \_ resourcezucationsettingdata-Instanz aus einem Ressourcenpool zugewiesen wird.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: CIM_ResourceAllocationFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960274"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="996ec-103">CIM \_ resourcezucationfrompool-Klasse</span><span class="sxs-lookup"><span data-stu-id="996ec-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="996ec-104">Stellt eine Zuordnung dar, in der eine [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Instanz aus einem Ressourcenpool zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="996ec-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="996ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="996ec-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="996ec-106">Member</span><span class="sxs-lookup"><span data-stu-id="996ec-106">Members</span></span>

<span data-ttu-id="996ec-107">Die **CIM \_ resourcezucationfrompool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="996ec-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="996ec-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996ec-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="996ec-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="996ec-109">Properties</span></span>

<span data-ttu-id="996ec-110">Die **CIM \_ resourcezucationfrompool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="996ec-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="996ec-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="996ec-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996ec-112">Datentyp: **CIM \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="996ec-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="996ec-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996ec-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996ec-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="996ec-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="996ec-115">Der Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="996ec-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="996ec-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="996ec-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996ec-117">Datentyp: **CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="996ec-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="996ec-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="996ec-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="996ec-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="996ec-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="996ec-120">Die Ressourcen Zuordnungs Daten.</span><span class="sxs-lookup"><span data-stu-id="996ec-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="996ec-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="996ec-121">Requirements</span></span>



| <span data-ttu-id="996ec-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="996ec-122">Requirement</span></span> | <span data-ttu-id="996ec-123">Wert</span><span class="sxs-lookup"><span data-stu-id="996ec-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996ec-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="996ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="996ec-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="996ec-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="996ec-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="996ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="996ec-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="996ec-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="996ec-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="996ec-128">Namespace</span></span><br/>                | <span data-ttu-id="996ec-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="996ec-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="996ec-130">MOF</span><span class="sxs-lookup"><span data-stu-id="996ec-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="996ec-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="996ec-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="996ec-132">DLL</span><span class="sxs-lookup"><span data-stu-id="996ec-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="996ec-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="996ec-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="996ec-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="996ec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996ec-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="996ec-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

