---
description: Stellt eine Beziehung zwischen einem Controller und einem vom Controller verwalteten logischen Gerät dar.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: CIM_ControlledBy-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863127"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="e04f3-103">CIM_ControlledBy-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="e04f3-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="e04f3-104">Stellt eine Beziehung zwischen einem Controller und einem vom Controller verwalteten logischen Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="e04f3-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e04f3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="e04f3-106">Member</span><span class="sxs-lookup"><span data-stu-id="e04f3-106">Members</span></span>

<span data-ttu-id="e04f3-107">Die **CIM \_ controlledby** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e04f3-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="e04f3-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e04f3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e04f3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e04f3-109">Properties</span></span>

<span data-ttu-id="e04f3-110">Die **CIM \_ controlledby** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e04f3-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e04f3-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="e04f3-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e04f3-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-114">Diese Eigenschaft beschreibt den Zugriff auf das Gerät über den Controller.</span><span class="sxs-lookup"><span data-stu-id="e04f3-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="e04f3-115">**Lesen** (2)</span><span class="sxs-lookup"><span data-stu-id="e04f3-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="e04f3-116">Schreib **geschützt (3** )</span><span class="sxs-lookup"><span data-stu-id="e04f3-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="e04f3-117">**NoAccess** (4)</span><span class="sxs-lookup"><span data-stu-id="e04f3-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e04f3-118">**Accesspriority**</span><span class="sxs-lookup"><span data-stu-id="e04f3-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e04f3-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-121">Die Priorität für den Zugriff des Geräts über den Controller.</span><span class="sxs-lookup"><span data-stu-id="e04f3-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="e04f3-122">Ein niedrigerer Wert weist auf eine höhere Priorität hin.</span><span class="sxs-lookup"><span data-stu-id="e04f3-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-123">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="e04f3-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e04f3-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-126">Gibt an, ob der Controller das Gerät aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e04f3-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e04f3-127">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e04f3-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e04f3-128">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="e04f3-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e04f3-129">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="e04f3-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e04f3-130">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e04f3-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-131">Datentyp: **CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="e04f3-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-133">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="e04f3-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-134">Der Controller.</span><span class="sxs-lookup"><span data-stu-id="e04f3-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-135">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e04f3-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-136">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e04f3-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-138">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="e04f3-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-139">Die logischen Geräte.</span><span class="sxs-lookup"><span data-stu-id="e04f3-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-140">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="e04f3-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e04f3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-143">Die Adresse des zugeordneten Geräts im Kontext des Controllers.</span><span class="sxs-lookup"><span data-stu-id="e04f3-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-144">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="e04f3-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e04f3-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-147">Qualifizierer: **Counter**</span><span class="sxs-lookup"><span data-stu-id="e04f3-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-148">Die Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e04f3-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="e04f3-149">Bei einer festen zurück setzung wird ein Gerät an den Initialisierungs-oder Startzustand zurückgegeben, in dem alle Informationen zum internen Gerätestatus und Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="e04f3-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-150">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="e04f3-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e04f3-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-153">Qualifizierer: **Counter**</span><span class="sxs-lookup"><span data-stu-id="e04f3-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-154">Die Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="e04f3-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="e04f3-155">Eine weiche zurück Setzung löscht den Gerätezustand oder die Daten nicht.</span><span class="sxs-lookup"><span data-stu-id="e04f3-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="e04f3-156">**Timeofdevicereset**</span><span class="sxs-lookup"><span data-stu-id="e04f3-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04f3-157">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e04f3-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e04f3-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e04f3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e04f3-159">Der Zeitpunkt, zu dem das Downstream-Gerät zuletzt vom Controller zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="e04f3-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e04f3-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e04f3-160">Requirements</span></span>



| <span data-ttu-id="e04f3-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e04f3-161">Requirement</span></span> | <span data-ttu-id="e04f3-162">Wert</span><span class="sxs-lookup"><span data-stu-id="e04f3-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04f3-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e04f3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e04f3-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e04f3-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e04f3-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e04f3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e04f3-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e04f3-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e04f3-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="e04f3-167">Namespace</span></span><br/>                | <span data-ttu-id="e04f3-168">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e04f3-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e04f3-169">MOF</span><span class="sxs-lookup"><span data-stu-id="e04f3-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e04f3-170"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e04f3-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e04f3-171">DLL</span><span class="sxs-lookup"><span data-stu-id="e04f3-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e04f3-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e04f3-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e04f3-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e04f3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04f3-174">**CIM-Geräte \_ Steuerung**</span><span class="sxs-lookup"><span data-stu-id="e04f3-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

