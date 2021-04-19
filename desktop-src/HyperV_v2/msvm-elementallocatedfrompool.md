---
description: Ordnet dem Ressourcenpool, aus dem Sie zugewiesen wurde, eine Instanz einer zugeordneten Ressource zu.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349970"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="46bf7-103">MSVM \_ elementenumeredfrompool-Klasse</span><span class="sxs-lookup"><span data-stu-id="46bf7-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="46bf7-104">Ordnet dem Ressourcenpool, aus dem Sie zugewiesen wurde, eine Instanz einer zugeordneten Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="46bf7-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="46bf7-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46bf7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46bf7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46bf7-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="46bf7-107">Member</span><span class="sxs-lookup"><span data-stu-id="46bf7-107">Members</span></span>

<span data-ttu-id="46bf7-108">Die **MSVM- \_ elementzuzuklasse** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="46bf7-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="46bf7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46bf7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46bf7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46bf7-110">Properties</span></span>

<span data-ttu-id="46bf7-111">Die **MSVM- \_ elementdeperedfrompool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46bf7-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46bf7-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="46bf7-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46bf7-113">Datentyp: **[ **CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="46bf7-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="46bf7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46bf7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46bf7-115">Qualifizierer: **außer Kraft** setzung, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="46bf7-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="46bf7-116">Der Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="46bf7-116">The resource pool.</span></span> <span data-ttu-id="46bf7-117">Diese Eigenschaft wird von [**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="46bf7-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="46bf7-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="46bf7-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46bf7-119">Datentyp: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="46bf7-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="46bf7-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46bf7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46bf7-121">Die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="46bf7-121">The allocated resource.</span></span> <span data-ttu-id="46bf7-122">Diese Eigenschaft wird von [**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="46bf7-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46bf7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46bf7-123">Remarks</span></span>

<span data-ttu-id="46bf7-124">Der Zugriff auf die **MSVM \_ elementzugedfrompool** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="46bf7-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46bf7-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="46bf7-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46bf7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46bf7-126">Requirements</span></span>



| <span data-ttu-id="46bf7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46bf7-127">Requirement</span></span> | <span data-ttu-id="46bf7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="46bf7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46bf7-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46bf7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="46bf7-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46bf7-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46bf7-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46bf7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="46bf7-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46bf7-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46bf7-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="46bf7-133">Namespace</span></span><br/>                | <span data-ttu-id="46bf7-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="46bf7-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46bf7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="46bf7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46bf7-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46bf7-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46bf7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="46bf7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46bf7-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46bf7-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46bf7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46bf7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46bf7-140">**CIM \_ elementzuzuedfrompool**</span><span class="sxs-lookup"><span data-stu-id="46bf7-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="46bf7-141">[**CIM \_ elementzuzuedfrompool**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46bf7-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="46bf7-142">**MSVM \_ Element Zuordnung (v1)**</span><span class="sxs-lookup"><span data-stu-id="46bf7-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="46bf7-143">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="46bf7-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

