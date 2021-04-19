---
description: Stellt den Ressourcen Status der switchbandbreite dar.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348377"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="3f6de-103">MSVM \_ ethernetzwitchbandwidthdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="3f6de-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="3f6de-104">Stellt den Ressourcen Status der switchbandbreite dar.</span><span class="sxs-lookup"><span data-stu-id="3f6de-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="3f6de-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f6de-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f6de-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="3f6de-107">Member</span><span class="sxs-lookup"><span data-stu-id="3f6de-107">Members</span></span>

<span data-ttu-id="3f6de-108">Die **MSVM \_ ethernetzwitchbandwidthdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f6de-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="3f6de-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f6de-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f6de-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f6de-110">Properties</span></span>

<span data-ttu-id="3f6de-111">Die **MSVM \_ ethernetzwitchbandwidthdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f6de-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f6de-112">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="3f6de-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f6de-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-115">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6de-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-116">Die maximale Bandbreite, die auf dem Switch verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3f6de-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-120">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3f6de-120">A short description of the object.</span></span> <span data-ttu-id="3f6de-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-122">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3f6de-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-125">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f6de-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-126">Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-127">**Defaultflowreservierung**</span><span class="sxs-lookup"><span data-stu-id="3f6de-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f6de-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-130">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6de-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-131">Die aktuelle absolute Bandbreite, die auf dem Switch für den Standard Ablauf reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-132">**Defaultflowreservationprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="3f6de-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f6de-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-135">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6de-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-136">Der aktuelle Prozentsatz der Bandbreite, die auf dem Switch für den Standard Ablauf reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-137">**Defaultflowweight**</span><span class="sxs-lookup"><span data-stu-id="3f6de-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-138">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f6de-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-140">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6de-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-141">Die aktuelle Gewichtung für den Standard Fluss auf dem Switch.</span><span class="sxs-lookup"><span data-stu-id="3f6de-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f6de-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-145">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3f6de-145">A description of the object.</span></span> <span data-ttu-id="3f6de-146">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3f6de-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-150">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-150">A display name for the object.</span></span> <span data-ttu-id="3f6de-151">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f6de-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-155">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="3f6de-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-156">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="3f6de-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3f6de-157">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="3f6de-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-161">Qualifizierer: **Key**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f6de-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-162">Der eindeutige Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f6de-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-163">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="3f6de-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-164">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f6de-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-166">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6de-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-167">Die aktuelle Bandbreite, die für den Switch reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-168">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="3f6de-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-171">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f6de-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-172">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="3f6de-172">The hosting system's creation class name.</span></span> <span data-ttu-id="3f6de-173">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="3f6de-174">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="3f6de-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6de-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3f6de-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f6de-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6de-177">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f6de-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f6de-178">Der Name des virtuellen Switchs, an den die zugeordnete Ressourcen Instanz gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f6de-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6de-179">Requirements</span></span>



| <span data-ttu-id="3f6de-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f6de-180">Requirement</span></span> | <span data-ttu-id="3f6de-181">Wert</span><span class="sxs-lookup"><span data-stu-id="3f6de-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6de-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f6de-182">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6de-183">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f6de-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f6de-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f6de-184">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6de-185">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f6de-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f6de-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f6de-186">Namespace</span></span><br/>                | <span data-ttu-id="3f6de-187">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f6de-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f6de-188">MOF</span><span class="sxs-lookup"><span data-stu-id="3f6de-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f6de-189"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3f6de-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f6de-190">DLL</span><span class="sxs-lookup"><span data-stu-id="3f6de-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f6de-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f6de-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

