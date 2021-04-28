---
description: 'Msvm_DeviceSAPImplementation-Klasse: Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.'
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
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112098"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="043d3-103">Msvm \_ DeviceSAPImplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="043d3-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="043d3-104">Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.</span><span class="sxs-lookup"><span data-stu-id="043d3-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="043d3-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="043d3-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="043d3-106">Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die in Verbindung stehen.</span><span class="sxs-lookup"><span data-stu-id="043d3-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="043d3-107">Jedes Gerät kann mehrere SAP-Geräte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="043d3-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="043d3-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="043d3-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="043d3-109">Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen.</span><span class="sxs-lookup"><span data-stu-id="043d3-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="043d3-110">Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="043d3-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="043d3-111">Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="043d3-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="043d3-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="043d3-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="043d3-113">Member</span><span class="sxs-lookup"><span data-stu-id="043d3-113">Members</span></span>

<span data-ttu-id="043d3-114">Die **Msvm \_ DeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="043d3-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="043d3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="043d3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="043d3-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="043d3-116">Properties</span></span>

<span data-ttu-id="043d3-117">Die **Msvm \_ DeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="043d3-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043d3-118">**Vorläufer**</span><span class="sxs-lookup"><span data-stu-id="043d3-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043d3-119">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="043d3-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="043d3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="043d3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043d3-121">Das logische Gerät.</span><span class="sxs-lookup"><span data-stu-id="043d3-121">The logical device.</span></span> <span data-ttu-id="043d3-122">Diese Eigenschaft wird von [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)geerbt.</span><span class="sxs-lookup"><span data-stu-id="043d3-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="043d3-123">**Abhängigen**</span><span class="sxs-lookup"><span data-stu-id="043d3-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043d3-124">Datentyp: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="043d3-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="043d3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="043d3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043d3-126">Der Mithilfe des logischen Geräts implementierte Dienstzugriffspunkt.</span><span class="sxs-lookup"><span data-stu-id="043d3-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="043d3-127">Diese Eigenschaft wird von [**CIM \_ DeviceSAPImplementation geerbt.**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)</span><span class="sxs-lookup"><span data-stu-id="043d3-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="043d3-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="043d3-128">Remarks</span></span>

<span data-ttu-id="043d3-129">Der Zugriff auf die **Msvm \_ DeviceSAPImplementation-Klasse** kann durch UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="043d3-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="043d3-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="043d3-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="043d3-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="043d3-131">Examples</span></span>

<span data-ttu-id="043d3-132">Weitere Informationen [finden Sie unter Abfragen von Netzwerkobjekten.](querying-networking-objects.md)</span><span class="sxs-lookup"><span data-stu-id="043d3-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="043d3-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="043d3-133">Requirements</span></span>



| <span data-ttu-id="043d3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="043d3-134">Requirement</span></span> | <span data-ttu-id="043d3-135">Wert</span><span class="sxs-lookup"><span data-stu-id="043d3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="043d3-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="043d3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="043d3-137">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="043d3-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="043d3-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="043d3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="043d3-139">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="043d3-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="043d3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="043d3-140">Namespace</span></span><br/>                | <span data-ttu-id="043d3-141">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="043d3-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="043d3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="043d3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043d3-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="043d3-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="043d3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="043d3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043d3-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="043d3-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="043d3-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="043d3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043d3-147">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="043d3-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="043d3-148">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="043d3-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

