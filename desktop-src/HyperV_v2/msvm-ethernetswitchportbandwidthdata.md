---
description: Stellt die Statusdaten der Port Bandbreite dar.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Msvm_EthernetSwitchPortBandwidthData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368139"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="e29ef-103">MSVM \_ ethernetzwitchportbandwidthdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="e29ef-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="e29ef-104">Stellt die Statusdaten der Port Bandbreite dar.</span><span class="sxs-lookup"><span data-stu-id="e29ef-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="e29ef-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e29ef-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e29ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e29ef-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="e29ef-107">Member</span><span class="sxs-lookup"><span data-stu-id="e29ef-107">Members</span></span>

<span data-ttu-id="e29ef-108">Die **MSVM \_ ethernetzwitchportbandwidthdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e29ef-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="e29ef-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e29ef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e29ef-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e29ef-110">Properties</span></span>

<span data-ttu-id="e29ef-111">Die **MSVM \_ ethernetzwitchportbandwidthdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e29ef-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e29ef-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e29ef-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e29ef-115">A short description of the object.</span></span> <span data-ttu-id="e29ef-116">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Feature Status" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-117">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="e29ef-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-120">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e29ef-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-121">Der Name der Unterklasse, die bei der Erstellung dieser Port Daten Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e29ef-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="e29ef-122">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ ethernettwitchportbandwidthdata" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-123">**Currentbandwidthreservationprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="e29ef-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e29ef-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e29ef-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-126">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e29ef-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-127">Der aktuelle Prozentsatz der Bandbreite, die für diesen Port reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="e29ef-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e29ef-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-131">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e29ef-131">A description of the object.</span></span> <span data-ttu-id="e29ef-132">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Port Bandbreite-Funktionsdaten" fest.</span><span class="sxs-lookup"><span data-stu-id="e29ef-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-133">**Geräteklassen Name**</span><span class="sxs-lookup"><span data-stu-id="e29ef-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-136">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e29ef-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-137">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e29ef-137">The scoping system's creation class name.</span></span> <span data-ttu-id="e29ef-138">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ ethernetzwitchport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e29ef-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-142">Qualifizierer: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e29ef-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-143">Die Geräte-ID des Ports, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="e29ef-144">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e29ef-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-148">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-148">A display name for the object.</span></span> <span data-ttu-id="e29ef-149">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Feature Status" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e29ef-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-153">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e29ef-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-154">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e29ef-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e29ef-155">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="e29ef-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-159">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e29ef-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-160">Eine Zeichenfolge, die diese Port Daten Instanz innerhalb des Bereichs des Schalters und des Ports eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e29ef-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="e29ef-161">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-162">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="e29ef-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-165">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e29ef-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-166">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e29ef-166">The scoping system's creation class name.</span></span> <span data-ttu-id="e29ef-167">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ virtualethernwitch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="e29ef-168">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="e29ef-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29ef-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e29ef-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e29ef-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29ef-171">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e29ef-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e29ef-172">Der Name des virtuellen Switches, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="e29ef-173">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e29ef-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e29ef-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e29ef-174">Requirements</span></span>



| <span data-ttu-id="e29ef-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e29ef-175">Requirement</span></span> | <span data-ttu-id="e29ef-176">Wert</span><span class="sxs-lookup"><span data-stu-id="e29ef-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e29ef-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e29ef-177">Minimum supported client</span></span><br/> | <span data-ttu-id="e29ef-178">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e29ef-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e29ef-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e29ef-179">Minimum supported server</span></span><br/> | <span data-ttu-id="e29ef-180">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e29ef-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e29ef-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="e29ef-181">Namespace</span></span><br/>                | <span data-ttu-id="e29ef-182">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e29ef-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e29ef-183">MOF</span><span class="sxs-lookup"><span data-stu-id="e29ef-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e29ef-184"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e29ef-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e29ef-185">DLL</span><span class="sxs-lookup"><span data-stu-id="e29ef-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e29ef-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e29ef-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

