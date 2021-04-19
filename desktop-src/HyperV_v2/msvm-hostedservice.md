---
description: Ordnet dem hostingcomputersystem einen Dienst zu.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Msvm_HostedService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360073"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="6938e-103">MSVM- \_ Klasse "hustedservice"</span><span class="sxs-lookup"><span data-stu-id="6938e-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="6938e-104">Ordnet dem hostingcomputersystem einen Dienst zu.</span><span class="sxs-lookup"><span data-stu-id="6938e-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="6938e-105">Instanzen von [**MSVM \_ virtualizationmanagementservice**](msvm-virtualsystemmanagementservice.md) können durch ihre Zuordnung zu einem Host ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6938e-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="6938e-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6938e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6938e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6938e-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6938e-108">Member</span><span class="sxs-lookup"><span data-stu-id="6938e-108">Members</span></span>

<span data-ttu-id="6938e-109">Die **MSVM-Klasse " \_ hustedservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6938e-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="6938e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6938e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6938e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6938e-111">Properties</span></span>

<span data-ttu-id="6938e-112">Die **MSVM-Klasse " \_ hustedservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6938e-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6938e-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6938e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6938e-114">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="6938e-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="6938e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6938e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6938e-116">Ein Verweis auf das hostingcomputersystem.</span><span class="sxs-lookup"><span data-stu-id="6938e-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="6938e-117">Diese Eigenschaft wird von [**CIM- \_ hustedservice**](/windows/desktop/CIMWin32Prov/cim-hostedservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6938e-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="6938e-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6938e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6938e-119">Datentyp: **[ **CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="6938e-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="6938e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6938e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6938e-121">Ein Verweis auf den gehosteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="6938e-121">A reference to the service being hosted.</span></span> <span data-ttu-id="6938e-122">Diese Eigenschaft wird von [**CIM- \_ hustedservice**](/windows/desktop/CIMWin32Prov/cim-hostedservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6938e-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6938e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6938e-123">Remarks</span></span>

<span data-ttu-id="6938e-124">Der Zugriff auf die **MSVM-Klasse " \_ hustedservice** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="6938e-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6938e-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6938e-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="6938e-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6938e-126">Examples</span></span>

<span data-ttu-id="6938e-127">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6938e-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6938e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6938e-128">Requirements</span></span>



| <span data-ttu-id="6938e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6938e-129">Requirement</span></span> | <span data-ttu-id="6938e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6938e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6938e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6938e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6938e-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6938e-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6938e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6938e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6938e-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6938e-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6938e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="6938e-135">Namespace</span></span><br/>                | <span data-ttu-id="6938e-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6938e-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6938e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6938e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6938e-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6938e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6938e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6938e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6938e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6938e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6938e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6938e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6938e-142">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="6938e-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="6938e-143">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="6938e-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="6938e-144">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="6938e-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

