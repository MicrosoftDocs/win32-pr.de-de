---
description: Stellt die Statusdaten für die Auslagerungs Funktion dar.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Msvm_EthernetSwitchPortOffloadData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373391"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="51695-103">MSVM \_ ethernezwitchportoffloaddata-Klasse</span><span class="sxs-lookup"><span data-stu-id="51695-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="51695-104">Stellt die Statusdaten für die Auslagerungs Funktion dar.</span><span class="sxs-lookup"><span data-stu-id="51695-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="51695-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51695-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51695-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51695-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="51695-107">Member</span><span class="sxs-lookup"><span data-stu-id="51695-107">Members</span></span>

<span data-ttu-id="51695-108">Die **MSVM \_ ethernezwitchportoffloaddata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51695-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="51695-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51695-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51695-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51695-110">Properties</span></span>

<span data-ttu-id="51695-111">Die **MSVM \_ ethernezwitchportoffloaddata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51695-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51695-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="51695-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51695-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51695-115">A short description of the object.</span></span> <span data-ttu-id="51695-116">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Feature Status" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51695-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="51695-117">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="51695-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-120">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="51695-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="51695-121">Der Name der Unterklasse, die bei der Erstellung dieser Port Daten Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51695-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="51695-122">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ ethernezwitchportoffloaddata" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51695-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="51695-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51695-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51695-126">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="51695-126">A description of the object.</span></span> <span data-ttu-id="51695-127">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Statusdaten für die Port Auslagerungs Funktion" dar.</span><span class="sxs-lookup"><span data-stu-id="51695-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="51695-128">**Geräteklassen Name**</span><span class="sxs-lookup"><span data-stu-id="51695-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-131">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="51695-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="51695-132">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="51695-132">The scoping system's creation class name.</span></span> <span data-ttu-id="51695-133">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ ethernetzwitchport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51695-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="51695-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="51695-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-137">Qualifizierer: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="51695-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="51695-138">Die Geräte-ID des Ports, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="51695-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="51695-139">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51695-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="51695-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="51695-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51695-143">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="51695-143">A display name for the object.</span></span> <span data-ttu-id="51695-144">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Feature Status" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51695-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="51695-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51695-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-148">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="51695-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="51695-149">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="51695-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="51695-150">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51695-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51695-151">**Iovoffloadusage**</span><span class="sxs-lookup"><span data-stu-id="51695-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-154">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-155">Die aktuelle Nutzung der e/a-Virtualisierung (IOV).</span><span class="sxs-lookup"><span data-stu-id="51695-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="51695-156">**Iovqueuepairusage**</span><span class="sxs-lookup"><span data-stu-id="51695-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-159">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-160">Die aktuelle Anzahl der Warteschlangen Paare, die vom Port verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51695-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="51695-161">**Iovvfdatapathactive**</span><span class="sxs-lookup"><span data-stu-id="51695-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-162">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51695-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51695-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-164">Qualifizierer: **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-165">Gibt an, ob der IOV VF-Datenpfad aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="51695-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="51695-166">**Iovvfid**</span><span class="sxs-lookup"><span data-stu-id="51695-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51695-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51695-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-169">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-170">Der aktuelle IOV VF-Bezeichner, der dem Port zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="51695-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="51695-171">Dies ist gültig, wenn **iovoffloadusage** nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="51695-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="51695-172">**Ipseccurrentoffloadsacount**</span><span class="sxs-lookup"><span data-stu-id="51695-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-173">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-175">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-176">Die aktuelle Anzahl der auf dem Port verwendeten Sicherheits Zuordnungs Slots (SA).</span><span class="sxs-lookup"><span data-stu-id="51695-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="51695-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="51695-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-180">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="51695-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="51695-181">Eine Zeichenfolge, die diese Port Daten Instanz innerhalb des Bereichs des Schalters und des Ports eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51695-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="51695-182">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51695-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="51695-183">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="51695-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-186">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="51695-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="51695-187">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="51695-187">The scoping system's creation class name.</span></span> <span data-ttu-id="51695-188">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt und ist immer auf "MSVM \_ virtualethernwitch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51695-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="51695-189">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="51695-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51695-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51695-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-192">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="51695-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="51695-193">Der Name des virtuellen Switches, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="51695-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="51695-194">Diese Eigenschaft wird von [**MSVM \_ ethernetportdata**](msvm-ethernetportdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51695-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="51695-195">**Vmmqaktivierte**</span><span class="sxs-lookup"><span data-stu-id="51695-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51695-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51695-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-198">Qualifizierer: **wmidataid** (9), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-199">Gibt an, ob vmmq aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="51695-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="51695-200">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51695-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-201">**Vmmqqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="51695-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-202">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-204">Qualifizierer: **wmidataid** (10), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-205">Gibt an, wie viele Warteschlangen für vrss/vmmq verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51695-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="51695-206">Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51695-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-207">**Vmqid**</span><span class="sxs-lookup"><span data-stu-id="51695-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-209">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-210">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-211">Die aktuelle Warteschlangen Kennung des virtuellen Computers, die dem Port zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="51695-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="51695-212">Dies ist gültig, wenn " **vmqoffloadusage** " nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="51695-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="51695-213">**Vmqoffloadusage**</span><span class="sxs-lookup"><span data-stu-id="51695-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-215">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="51695-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51695-216">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-217">Die aktuelle Virtual Machine Queue (VMQ)-Auslastungs Auslastung.</span><span class="sxs-lookup"><span data-stu-id="51695-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="51695-218">**Vrssaktivierte**</span><span class="sxs-lookup"><span data-stu-id="51695-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51695-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51695-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-221">Qualifizierer: **wmidataid** (8), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-222">Gibt an, ob vrss aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="51695-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="51695-223">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51695-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-224">**Vrssexcludeprimaryprocessor**</span><span class="sxs-lookup"><span data-stu-id="51695-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-225">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51695-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51695-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-227">Qualifizierer: **wmidataid** (13), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-228">Gibt an, ob die primäre VMQ-CPU von der vrss/vmmq-dereferenzierungstabelle ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="51695-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="51695-229">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="51695-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-230">**Vrssindependenthostverteilung**</span><span class="sxs-lookup"><span data-stu-id="51695-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51695-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51695-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-233">Qualifizierer: **wmidataid** (14), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-234">Gibt an, ob die Host seitige vrss-/vmmq-Verteilung stattfindet, unabhängig von den RSS-Einstellungen der virtuellen NIC.</span><span class="sxs-lookup"><span data-stu-id="51695-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="51695-235">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="51695-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-236">**Vrssminqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="51695-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-237">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-239">Qualifizierer: **wmidataid** (11), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-240">Gibt die Mindestanzahl von Warteschlangen an, die für vrss/vmmq verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51695-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="51695-241">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="51695-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-242">**Vrssqueueschedulingmode**</span><span class="sxs-lookup"><span data-stu-id="51695-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-243">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-245">Qualifizierer: **wmidataid** (12), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-246">Gibt an, wie vrss/vmmq-Warteschlangen an verschiedene Host Prozessoren geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="51695-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="51695-247">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="51695-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="51695-248">**Vrssvmbuschannelaffinitypolicy**</span><span class="sxs-lookup"><span data-stu-id="51695-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51695-249">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51695-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51695-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51695-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51695-251">Qualifizierer: **wmidataid** (15), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="51695-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="51695-252">Gibt an, wie VMBus-Kanäle Host Prozessoren zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="51695-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="51695-253">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="51695-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51695-254">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51695-254">Requirements</span></span>



| <span data-ttu-id="51695-255">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51695-255">Requirement</span></span> | <span data-ttu-id="51695-256">Wert</span><span class="sxs-lookup"><span data-stu-id="51695-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51695-257">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51695-257">Minimum supported client</span></span><br/> | <span data-ttu-id="51695-258">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51695-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="51695-259">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51695-259">Minimum supported server</span></span><br/> | <span data-ttu-id="51695-260">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51695-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51695-261">Namespace</span><span class="sxs-lookup"><span data-stu-id="51695-261">Namespace</span></span><br/>                | <span data-ttu-id="51695-262">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="51695-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51695-263">MOF</span><span class="sxs-lookup"><span data-stu-id="51695-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51695-264"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51695-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51695-265">DLL</span><span class="sxs-lookup"><span data-stu-id="51695-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51695-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51695-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

