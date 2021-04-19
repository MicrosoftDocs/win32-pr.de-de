---
description: Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350315"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="49e33-103">MSVM- \_ devicesapimplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="49e33-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="49e33-104">Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung.</span><span class="sxs-lookup"><span data-stu-id="49e33-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="49e33-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="49e33-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="49e33-106">Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="49e33-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="49e33-107">Jedes Gerät kann mehr als ein SAP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="49e33-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="49e33-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="49e33-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="49e33-109">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49e33-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="49e33-110">Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="49e33-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="49e33-111">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49e33-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e33-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="49e33-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="49e33-113">Member</span><span class="sxs-lookup"><span data-stu-id="49e33-113">Members</span></span>

<span data-ttu-id="49e33-114">Die **MSVM \_ devicesapimplementation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="49e33-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="49e33-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49e33-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49e33-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49e33-116">Properties</span></span>

<span data-ttu-id="49e33-117">Die **MSVM \_ devicesapimplementation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49e33-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49e33-118">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="49e33-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49e33-119">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="49e33-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="49e33-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49e33-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49e33-121">Das logische Gerät.</span><span class="sxs-lookup"><span data-stu-id="49e33-121">The logical device.</span></span> <span data-ttu-id="49e33-122">Diese Eigenschaft wird von CIM-Geräte- [**\_ Implementierung**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49e33-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="49e33-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="49e33-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49e33-124">Datentyp: **[ **CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="49e33-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="49e33-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49e33-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49e33-126">Der über das logische Gerät implementierte Dienst Zugriffspunkt.</span><span class="sxs-lookup"><span data-stu-id="49e33-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="49e33-127">Diese Eigenschaft wird von CIM-Geräte- [**\_ Implementierung**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49e33-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49e33-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49e33-128">Remarks</span></span>

<span data-ttu-id="49e33-129">Der Zugriff auf die **MSVM-Klasse \_ devicesapimplementation** kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="49e33-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="49e33-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="49e33-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="49e33-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49e33-131">Examples</span></span>

<span data-ttu-id="49e33-132">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="49e33-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49e33-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49e33-133">Requirements</span></span>



| <span data-ttu-id="49e33-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49e33-134">Requirement</span></span> | <span data-ttu-id="49e33-135">Wert</span><span class="sxs-lookup"><span data-stu-id="49e33-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e33-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49e33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="49e33-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e33-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="49e33-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49e33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="49e33-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e33-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49e33-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="49e33-140">Namespace</span></span><br/>                | <span data-ttu-id="49e33-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="49e33-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="49e33-142">MOF</span><span class="sxs-lookup"><span data-stu-id="49e33-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49e33-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="49e33-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49e33-144">DLL</span><span class="sxs-lookup"><span data-stu-id="49e33-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49e33-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49e33-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="49e33-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49e33-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e33-147">**CIM-Geräte \_ Implementierung**</span><span class="sxs-lookup"><span data-stu-id="49e33-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="49e33-148">**CIM-Geräte \_ Implementierung**</span><span class="sxs-lookup"><span data-stu-id="49e33-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

