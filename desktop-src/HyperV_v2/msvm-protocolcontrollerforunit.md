---
description: Diese Zuordnung gibt an, dass eine Unterklasse des logischen Geräts (z. b. ein Speicher Volume) über einen bestimmten Protokoll Controller verbunden ist.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345854"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="3899f-103">MSVM \_ protocolcontrollerforunit-Klasse</span><span class="sxs-lookup"><span data-stu-id="3899f-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="3899f-104">Diese Zuordnung gibt an, dass eine Unterklasse des logischen Geräts (z. b. ein Speicher Volume) über einen bestimmten Protokoll Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="3899f-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="3899f-105">In vielen Situationen (z. b. bei der Speicher-LUN-Maskierung) können viele dieser Zuordnungen verwendet werden, um sich auf unterschiedliche Objekte zu beziehen.</span><span class="sxs-lookup"><span data-stu-id="3899f-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="3899f-106">Daher wurden Unterklassen definiert, um die Enumeration der Zuordnungen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="3899f-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="3899f-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3899f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3899f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3899f-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="3899f-109">Member</span><span class="sxs-lookup"><span data-stu-id="3899f-109">Members</span></span>

<span data-ttu-id="3899f-110">Die **MSVM \_ protocolcontrollerforunit** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3899f-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="3899f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3899f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3899f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3899f-112">Properties</span></span>

<span data-ttu-id="3899f-113">Die **MSVM \_ protocolcontrollerforunit** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3899f-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3899f-114">**Accesspriority**</span><span class="sxs-lookup"><span data-stu-id="3899f-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-115">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3899f-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-117">Die Priorität, die für den Zugriff auf das Gerät über diesen Controller eingeräumt wird.</span><span class="sxs-lookup"><span data-stu-id="3899f-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="3899f-118">Der Pfad mit der höchsten Priorität weist den niedrigsten Wert für diesen Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="3899f-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="3899f-119">Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="3899f-120">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="3899f-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-121">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3899f-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-123">Gibt an, ob der Controller aktiv auf das Gerät zugreift (2) oder nicht (3).</span><span class="sxs-lookup"><span data-stu-id="3899f-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="3899f-124">Außerdem kann der Wert 0 (unbekannt) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3899f-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="3899f-125">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Protokoll Controller oder durch den Zugriff darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3899f-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="3899f-126">Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="3899f-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3899f-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3899f-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="3899f-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3899f-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inaktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="3899f-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3899f-130">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3899f-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-131">Datentyp: **[ **CIM \_ protocolcontroller**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="3899f-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-133">Der Protokoll Controller.</span><span class="sxs-lookup"><span data-stu-id="3899f-133">The protocol controller.</span></span> <span data-ttu-id="3899f-134">Diese Klasse wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3899f-135">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3899f-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-136">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="3899f-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-138">Das kontrollierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="3899f-138">The controlled device.</span></span> <span data-ttu-id="3899f-139">Diese Klasse wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3899f-140">**Deviceaccess**</span><span class="sxs-lookup"><span data-stu-id="3899f-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3899f-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-143">Die Zugriffsrechte, die dem Gerät über diesen Controller erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="3899f-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="3899f-144">Diese Klasse wird von **CIM \_ protocolcontrollerforunit** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="3899f-145">Wert</span><span class="sxs-lookup"><span data-stu-id="3899f-145">Value</span></span>                                                                               | <span data-ttu-id="3899f-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3899f-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3899f-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="3899f-148">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="3899f-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="3899f-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="3899f-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3899f-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="3899f-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="3899f-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="3899f-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="3899f-154">Kein Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3899f-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="3899f-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="3899f-156">DMTF reserviert</span><span class="sxs-lookup"><span data-stu-id="3899f-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="3899f-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="3899f-158">Anbieter reserviert</span><span class="sxs-lookup"><span data-stu-id="3899f-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3899f-159">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="3899f-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3899f-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3899f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3899f-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3899f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3899f-162">Die Adresse des zugeordneten Geräts im Zusammenhang mit dem Vorgänger Controller.</span><span class="sxs-lookup"><span data-stu-id="3899f-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="3899f-163">Diese Klasse wird von **CIM \_ protocolcontrollerfordevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3899f-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3899f-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3899f-164">Remarks</span></span>

<span data-ttu-id="3899f-165">Der Zugriff auf die **MSVM \_ protocolcontrollerforunit** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3899f-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3899f-166">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3899f-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3899f-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3899f-167">Requirements</span></span>



| <span data-ttu-id="3899f-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3899f-168">Requirement</span></span> | <span data-ttu-id="3899f-169">Wert</span><span class="sxs-lookup"><span data-stu-id="3899f-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3899f-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3899f-170">Minimum supported client</span></span><br/> | <span data-ttu-id="3899f-171">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3899f-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3899f-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3899f-172">Minimum supported server</span></span><br/> | <span data-ttu-id="3899f-173">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3899f-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3899f-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="3899f-174">Namespace</span></span><br/>                | <span data-ttu-id="3899f-175">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3899f-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3899f-176">MOF</span><span class="sxs-lookup"><span data-stu-id="3899f-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3899f-177"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3899f-178">DLL</span><span class="sxs-lookup"><span data-stu-id="3899f-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3899f-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3899f-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3899f-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3899f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3899f-181">**CIM \_ protocolcontrollerforunit**</span><span class="sxs-lookup"><span data-stu-id="3899f-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="3899f-182">[**CIM \_ protocolcontrollerforunit**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3899f-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3899f-183">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="3899f-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

