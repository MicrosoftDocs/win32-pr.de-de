---
description: Ordnet dem Ressourcenpool, aus dem Sie zugeordnet ist, eine Instanz einer Ressourcenzuweisung zu.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349487"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="6e19c-103">MSVM \_ resourcezucationfrompool-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e19c-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="6e19c-104">Ordnet dem Ressourcenpool, aus dem Sie zugeordnet ist, eine Instanz einer Ressourcenzuweisung zu.</span><span class="sxs-lookup"><span data-stu-id="6e19c-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="6e19c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e19c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e19c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e19c-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6e19c-107">Member</span><span class="sxs-lookup"><span data-stu-id="6e19c-107">Members</span></span>

<span data-ttu-id="6e19c-108">Die **MSVM \_ resourcezucationfrompool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e19c-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="6e19c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e19c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e19c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e19c-110">Properties</span></span>

<span data-ttu-id="6e19c-111">Die **MSVM \_ resourcezucationfrompool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e19c-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e19c-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6e19c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e19c-113">Datentyp: **[ **CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6e19c-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="6e19c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e19c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e19c-115">Qualifizierer: **außer Kraft** setzung, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="6e19c-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="6e19c-116">Der Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="6e19c-116">The resource pool.</span></span> <span data-ttu-id="6e19c-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationfrompool**](/previous-versions//cc150673(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e19c-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6e19c-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6e19c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e19c-119">Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="6e19c-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="6e19c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e19c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e19c-121">Die Ressourcenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="6e19c-121">The resource allocation.</span></span> <span data-ttu-id="6e19c-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationfrompool**](/previous-versions//cc150673(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e19c-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e19c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e19c-123">Remarks</span></span>

<span data-ttu-id="6e19c-124">Der Zugriff auf die **MSVM \_ resourcezucationfrompool** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="6e19c-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6e19c-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6e19c-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e19c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e19c-126">Requirements</span></span>



| <span data-ttu-id="6e19c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e19c-127">Requirement</span></span> | <span data-ttu-id="6e19c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6e19c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e19c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e19c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6e19c-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e19c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6e19c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e19c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6e19c-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e19c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e19c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e19c-133">Namespace</span></span><br/>                | <span data-ttu-id="6e19c-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e19c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6e19c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6e19c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e19c-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e19c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e19c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6e19c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e19c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e19c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e19c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e19c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e19c-140">**CIM \_ resourcezucationfrompool**</span><span class="sxs-lookup"><span data-stu-id="6e19c-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="6e19c-141">[**CIM \_ resourcezucationfrompool**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e19c-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6e19c-142">**MSVM \_ resourcezucationfrompool (v1)**</span><span class="sxs-lookup"><span data-stu-id="6e19c-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="6e19c-143">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="6e19c-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

