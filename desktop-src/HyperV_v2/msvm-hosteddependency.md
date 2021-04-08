---
description: Ordnet dem Computersystem Objekt, das das physische Host System darstellt, eine Instanz eines virtuellen Computers zu.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862072"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="92f6b-103">MSVM- \_ Klasse "husteddependenz"</span><span class="sxs-lookup"><span data-stu-id="92f6b-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="92f6b-104">Ordnet dem Computersystem Objekt, das das physische Host System darstellt, eine Instanz eines virtuellen Computers zu.</span><span class="sxs-lookup"><span data-stu-id="92f6b-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="92f6b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92f6b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92f6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="92f6b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="92f6b-107">Member</span><span class="sxs-lookup"><span data-stu-id="92f6b-107">Members</span></span>

<span data-ttu-id="92f6b-108">Die **MSVM-Klasse " \_ husteddependenz** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="92f6b-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="92f6b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92f6b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92f6b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92f6b-110">Properties</span></span>

<span data-ttu-id="92f6b-111">Die **MSVM-Klasse " \_ husteddepend** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92f6b-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92f6b-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="92f6b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f6b-113">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="92f6b-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="92f6b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92f6b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92f6b-115">Ein Verweis auf das hostingcomputersystem.</span><span class="sxs-lookup"><span data-stu-id="92f6b-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="92f6b-116">Diese Eigenschaft wird von [**CIM- \_ hupabhängigkeit**](/previous-versions//cc136861(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="92f6b-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="92f6b-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="92f6b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f6b-118">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="92f6b-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="92f6b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92f6b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92f6b-120">Ein Verweis auf den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="92f6b-120">A reference to the virtual machine.</span></span> <span data-ttu-id="92f6b-121">Diese Eigenschaft wird von [**CIM- \_ hupabhängigkeit**](/previous-versions//cc136861(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="92f6b-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92f6b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92f6b-122">Remarks</span></span>

<span data-ttu-id="92f6b-123">Der Zugriff auf die **MSVM-Klasse " \_ husteddepend** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="92f6b-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="92f6b-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="92f6b-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="92f6b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92f6b-125">Requirements</span></span>



| <span data-ttu-id="92f6b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92f6b-126">Requirement</span></span> | <span data-ttu-id="92f6b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="92f6b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92f6b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92f6b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="92f6b-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92f6b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="92f6b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92f6b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="92f6b-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92f6b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92f6b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="92f6b-132">Namespace</span></span><br/>                | <span data-ttu-id="92f6b-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="92f6b-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="92f6b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="92f6b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92f6b-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="92f6b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92f6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="92f6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92f6b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92f6b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92f6b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92f6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f6b-139">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="92f6b-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="92f6b-140">[**CIM- \_ hubabhängigkeit**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92f6b-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92f6b-141">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="92f6b-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

