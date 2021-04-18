---
description: Stellt einen Dienst für virtuelle Geräte der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344255"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="f378f-103">MSVM \_ virtualsystemresourcecomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="f378f-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="f378f-104">Stellt einen Dienst für virtuelle Geräte der Microsoft Windows Hyper-V-Plattform dar.</span><span class="sxs-lookup"><span data-stu-id="f378f-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="f378f-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f378f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f378f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f378f-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="f378f-107">Member</span><span class="sxs-lookup"><span data-stu-id="f378f-107">Members</span></span>

<span data-ttu-id="f378f-108">Die **MSVM \_ virtualsystemresourcecomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f378f-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f378f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f378f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f378f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f378f-110">Properties</span></span>

<span data-ttu-id="f378f-111">Die **MSVM \_ virtualsystemresourcecomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f378f-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f378f-112">**Additionalclassnames**</span><span class="sxs-lookup"><span data-stu-id="f378f-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f378f-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f378f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-115">Ein Array von Zeichen folgen, das zusätzliche nicht Zuordnungs Klassen enthält, die von dieser **MSVM \_ virtualsystemresourcecomponent** -Instanz bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f378f-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="f378f-116">Diese Klassen müssen von weder [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) noch [**CIM \_ resourcezucationsettingdata abgeleitet werden**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="f378f-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="f378f-117">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="f378f-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f378f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-120">Eine GUID, die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt.</span><span class="sxs-lookup"><span data-stu-id="f378f-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="f378f-121">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f378f-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f378f-122">**Context**</span><span class="sxs-lookup"><span data-stu-id="f378f-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f378f-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-125">Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f378f-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="f378f-126">Dieser Wert wird im *dwClsContext* -Parameter an [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben.</span><span class="sxs-lookup"><span data-stu-id="f378f-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="f378f-127">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f378f-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-128">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="f378f-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-131">**True** , wenn diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f378f-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="f378f-132">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f378f-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-133">**Hotadd**</span><span class="sxs-lookup"><span data-stu-id="f378f-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-136">**True** , wenn diese Instanz einem virtuellen Computer hinzugefügt werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f378f-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f378f-137">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="f378f-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-138">**Baum verschieben**</span><span class="sxs-lookup"><span data-stu-id="f378f-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-141">**True** , wenn diese Instanz von einem virtuellen Computer entfernt werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f378f-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f378f-142">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="f378f-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="f378f-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f378f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f378f-146">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f378f-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f378f-147">Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f378f-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="f378f-148">Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version".</span><span class="sxs-lookup"><span data-stu-id="f378f-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="f378f-149">Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="f378f-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="f378f-150">Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f378f-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f378f-151">**Type**</span><span class="sxs-lookup"><span data-stu-id="f378f-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f378f-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f378f-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f378f-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f378f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f378f-154">Die Beziehung des WMI-Objekts, das hier mit dem virtuellen Gerät beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f378f-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="f378f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="f378f-156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f378f-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="f378f-157"><dt>**"Nicht änderbar"**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="f378f-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="f378f-159">Singleton ist ein WMI-Objekt der obersten Ebene, das 1:1 an ein virtuelles Gerät gebunden ist und nur einmal pro virtuellem Computer vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="f378f-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="f378f-160">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f378f-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="f378f-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f378f-162">MultiInstance ist ein WMI-Objekt der obersten Ebene, das mehrmals pro virtuellem Computer vorhanden sein kann und 1:1 an ein virtuelles Gerät gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f378f-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="f378f-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="f378f-164">Bei dem Subgerät handelt es sich um ein WMI-Objekt, das nicht über einen übergeordneten Verweis verfügt, sondern nur von einem virtuellen Gerät gesteuert wird, das nur einmal pro virtuellem Computer</span><span class="sxs-lookup"><span data-stu-id="f378f-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="f378f-165">Das WMI-Objekt kann jedoch vielfachen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f378f-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f378f-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f378f-166">Remarks</span></span>

<span data-ttu-id="f378f-167">Der Zugriff auf die **MSVM \_ virtualsystemresourcecomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="f378f-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f378f-168">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f378f-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f378f-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f378f-169">Requirements</span></span>



| <span data-ttu-id="f378f-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f378f-170">Requirement</span></span> | <span data-ttu-id="f378f-171">Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f378f-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f378f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f378f-173">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f378f-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f378f-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f378f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f378f-175">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f378f-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f378f-176">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f378f-176">End of client support</span></span><br/>    | <span data-ttu-id="f378f-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f378f-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f378f-178">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f378f-178">End of server support</span></span><br/>    | <span data-ttu-id="f378f-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f378f-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f378f-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="f378f-180">Namespace</span></span><br/>                | <span data-ttu-id="f378f-181">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f378f-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f378f-182">MOF</span><span class="sxs-lookup"><span data-stu-id="f378f-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f378f-183"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f378f-184">DLL</span><span class="sxs-lookup"><span data-stu-id="f378f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f378f-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f378f-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f378f-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f378f-187">**MSVM \_ virtualizationcomponent**</span><span class="sxs-lookup"><span data-stu-id="f378f-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="f378f-188">**MSVM \_ virtualizationcomponent**</span><span class="sxs-lookup"><span data-stu-id="f378f-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

