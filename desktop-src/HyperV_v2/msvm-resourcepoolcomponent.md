---
description: Stellt ein Ressourcenpool Element der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350295"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="1cf74-103">MSVM \_ resourcepoolcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="1cf74-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="1cf74-104">Stellt ein Ressourcenpool Element der Microsoft Windows Hyper-V-Plattform dar.</span><span class="sxs-lookup"><span data-stu-id="1cf74-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="1cf74-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cf74-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf74-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cf74-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="1cf74-107">Member</span><span class="sxs-lookup"><span data-stu-id="1cf74-107">Members</span></span>

<span data-ttu-id="1cf74-108">Die **MSVM \_ resourcepoolcomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1cf74-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1cf74-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cf74-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cf74-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cf74-110">Properties</span></span>

<span data-ttu-id="1cf74-111">Die **MSVM \_ resourcepoolcomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cf74-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cf74-112">**Zuordnung von "Zuweisung Name"**</span><span class="sxs-lookup"><span data-stu-id="1cf74-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-115">Der Name der von [**CIM \_ allocationfunktionalitäten**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) abgeleiteten Klasse, die die Zuordnungs Funktionen dieses Ressourcenpools beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-116">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="1cf74-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-119">Eine **GUID** , die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="1cf74-120">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-121">**Context**</span><span class="sxs-lookup"><span data-stu-id="1cf74-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1cf74-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-124">Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cf74-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="1cf74-125">Dieser Wert wird im *dwClsContext* -Parameter an **cokreateingestance** übergeben.</span><span class="sxs-lookup"><span data-stu-id="1cf74-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="1cf74-126">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-127">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="1cf74-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1cf74-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-130">**True** , wenn diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="1cf74-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="1cf74-131">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-132">**Maxparser-Pools**</span><span class="sxs-lookup"><span data-stu-id="1cf74-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-133">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1cf74-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-135">Die maximale Anzahl von übergeordneten Ressourcenpools, die von einem untergeordneten Pool unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1cf74-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="1cf74-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-139">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1cf74-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-140">Eine sprachneutrale Zeichenfolge, die das Element eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1cf74-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="1cf74-141">Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version".</span><span class="sxs-lookup"><span data-stu-id="1cf74-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="1cf74-142">Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="1cf74-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="1cf74-143">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-144">**Physicalenviceclassname**</span><span class="sxs-lookup"><span data-stu-id="1cf74-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-147">Der Name der von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) abgeleiteten Klasse, die das physische Gerät implementiert, von dem dieser Pool Ressourcen freigibt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="1cf74-148">Diese Eigenschaft kann **null** sein, wenn die von diesem Pool zugewiesene virtuelle Geräteklasse mit der Klasse des physischen Geräts identisch ist.</span><span class="sxs-lookup"><span data-stu-id="1cf74-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-149">**Resourcepoolclassname**</span><span class="sxs-lookup"><span data-stu-id="1cf74-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-152">Der Name der Klasse, die von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85)) abgeleitet wird und den Ressourcenpool implementiert.</span><span class="sxs-lookup"><span data-stu-id="1cf74-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-153">**Resourcepoolsettingdataclassname**</span><span class="sxs-lookup"><span data-stu-id="1cf74-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-156">Der Name der von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) abgeleiteten Klasse, die die nicht Zuordnungs bezogenen Einstellungen des Ressourcenpools beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="1cf74-157">**Wmifactoriyclsid**</span><span class="sxs-lookup"><span data-stu-id="1cf74-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf74-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cf74-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf74-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cf74-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf74-160">Eine **GUID** , die den Klassen Bezeichner der WMI-Objektfactory der Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="1cf74-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cf74-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cf74-161">Remarks</span></span>

<span data-ttu-id="1cf74-162">Der Zugriff auf die **MSVM \_ resourcepoolcomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1cf74-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1cf74-163">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1cf74-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf74-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cf74-164">Requirements</span></span>



| <span data-ttu-id="1cf74-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cf74-165">Requirement</span></span> | <span data-ttu-id="1cf74-166">Wert</span><span class="sxs-lookup"><span data-stu-id="1cf74-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf74-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1cf74-167">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf74-168">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1cf74-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1cf74-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1cf74-169">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf74-170">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1cf74-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cf74-171">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1cf74-171">End of client support</span></span><br/>    | <span data-ttu-id="1cf74-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1cf74-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1cf74-173">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1cf74-173">End of server support</span></span><br/>    | <span data-ttu-id="1cf74-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1cf74-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1cf74-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cf74-175">Namespace</span></span><br/>                | <span data-ttu-id="1cf74-176">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1cf74-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1cf74-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1cf74-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cf74-178"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1cf74-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cf74-179">DLL</span><span class="sxs-lookup"><span data-stu-id="1cf74-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cf74-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cf74-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cf74-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cf74-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf74-182">**MSVM \_ virtualizationcomponent**</span><span class="sxs-lookup"><span data-stu-id="1cf74-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="1cf74-183">**MSVM \_ virtualizationcomponent**</span><span class="sxs-lookup"><span data-stu-id="1cf74-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

