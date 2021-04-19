---
description: Stellt die Einstellungsdaten für die Port Auslagerung dar.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355480"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="8b42a-103">MSVM \_ ethernezwitchportoffloadsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b42a-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="8b42a-104">Stellt die Einstellungsdaten für die Port Auslagerung dar.</span><span class="sxs-lookup"><span data-stu-id="8b42a-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="8b42a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b42a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b42a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b42a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="8b42a-107">Member</span><span class="sxs-lookup"><span data-stu-id="8b42a-107">Members</span></span>

<span data-ttu-id="8b42a-108">Die **MSVM \_ ethernezwitchportoffloadsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b42a-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8b42a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b42a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b42a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b42a-110">Properties</span></span>

<span data-ttu-id="8b42a-111">Die **MSVM \_ ethernezwitchportoffloadsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b42a-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b42a-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8b42a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b42a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b42a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b42a-115">A short description of the object.</span></span> <span data-ttu-id="8b42a-116">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b42a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b42a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b42a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b42a-120">A description of the object.</span></span> <span data-ttu-id="8b42a-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Einstellung für die Funktion der Port Abladung" dar.</span><span class="sxs-lookup"><span data-stu-id="8b42a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8b42a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b42a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b42a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-125">A display name for the object.</span></span> <span data-ttu-id="8b42a-126">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8b42a-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b42a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b42a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="8b42a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="8b42a-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8b42a-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-133">**Iovinterruptmode**</span><span class="sxs-lookup"><span data-stu-id="8b42a-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-136">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-137">Der Wert für die Unterbrechungs Moderation für die e/a-Virtualisierung (IOV).</span><span class="sxs-lookup"><span data-stu-id="8b42a-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="8b42a-138">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="8b42a-139">**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="8b42a-140">**Adaptive** (1)</span><span class="sxs-lookup"><span data-stu-id="8b42a-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="8b42a-141">**Aus** (2)</span><span class="sxs-lookup"><span data-stu-id="8b42a-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="8b42a-142">**Niedrig** (100)</span><span class="sxs-lookup"><span data-stu-id="8b42a-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="8b42a-143">**Mittel** (200)</span><span class="sxs-lookup"><span data-stu-id="8b42a-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8b42a-144">**Hoch** (300)</span><span class="sxs-lookup"><span data-stu-id="8b42a-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b42a-145">**Iovoffloadweight**</span><span class="sxs-lookup"><span data-stu-id="8b42a-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-148">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-149">Die Gewichtung, die diesem Port für die e/a-Virtualisierung (IOV) zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8b42a-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="8b42a-150">Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von IOV-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8b42a-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="8b42a-151">Wenn Sie die **iovoffloadweight** -Eigenschaft auf 0 festlegen, wird die IOV-Auslagerung auf dem Port deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b42a-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="8b42a-152">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-153">**Iovqueuepairrsangefordert**</span><span class="sxs-lookup"><span data-stu-id="8b42a-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-156">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-157">Die Anzahl der für diesen Port angeforderten Warteschlangen Paare für die e/a-Virtualisierung (IOV).</span><span class="sxs-lookup"><span data-stu-id="8b42a-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="8b42a-158">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8b42a-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-159">**Ipmencoffloadlimit**</span><span class="sxs-lookup"><span data-stu-id="8b42a-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-162">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-163">Die maximale Anzahl von Auslagerungs Slots (Security Association, SA), die vom Port zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="8b42a-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-164">**Packetdirectmoderationcount**</span><span class="sxs-lookup"><span data-stu-id="8b42a-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-167">Qualifizierer: **wmidataid** (7), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-168">Der Wert der Unterbrechungs Moderations Moderation für "Packet Direct" (PD). Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-169">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-170">**Packetdirectmoderationinterval**</span><span class="sxs-lookup"><span data-stu-id="8b42a-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-173">Qualifizierer: **wmidataid** (8), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-174">Der Wert für das interruptermoderationsintervall für "Packet Direct" (PD). Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-175">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-176">**Packetdirectnumprocs**</span><span class="sxs-lookup"><span data-stu-id="8b42a-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-179">Qualifizierer: **wmidataid** (6), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-180">Die Anzahl der Prozessoren, die vom Host für die Verarbeitung von Paketen verwendet werden, die von diesem Port im Paket direkt Modus gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b42a-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="8b42a-181">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8b42a-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-182">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-183">**Vmmqaktivierte**</span><span class="sxs-lookup"><span data-stu-id="8b42a-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b42a-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-186">Qualifizierer: **wmidataid** (10), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-187">Aktivieren Sie vmmq-Auslagerung, wenn dies von Hardware unterstützt wird. Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="8b42a-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-188">Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-189">**Vmmqqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="8b42a-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-190">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-192">Qualifizierer: **wmidataid** (11), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-193">Die Anzahl der Warteschlangen, die bei Aktivierung von vrss zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="8b42a-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="8b42a-194">Der Standardwert ist 16.</span><span class="sxs-lookup"><span data-stu-id="8b42a-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-195">Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-196">**Vmqoffloadweight**</span><span class="sxs-lookup"><span data-stu-id="8b42a-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-199">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-200">Die Gewichtung, die diesem Port für die VM-Offloads (Virtual Machine Queue, VMQ) zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8b42a-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="8b42a-201">Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von VMQ-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8b42a-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="8b42a-202">Wenn Sie die **vmqoffloadweight** -Eigenschaft auf 0 festlegen, wird VMQ auf dem Port deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b42a-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="8b42a-203">Der Standard ist 100.</span><span class="sxs-lookup"><span data-stu-id="8b42a-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="8b42a-204">**Vrssaktivierte**</span><span class="sxs-lookup"><span data-stu-id="8b42a-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-205">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b42a-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-206">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-207">Qualifizierer: **wmidataid** (9), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-208">Aktivieren Sie vrss.</span><span class="sxs-lookup"><span data-stu-id="8b42a-208">Enable VRSS.</span></span> <span data-ttu-id="8b42a-209">Der Standardwert ist "True".</span><span class="sxs-lookup"><span data-stu-id="8b42a-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-210">Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b42a-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-211">**Vrssexcludeprimaryprocessor**</span><span class="sxs-lookup"><span data-stu-id="8b42a-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-212">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b42a-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-213">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-214">Qualifizierer: **wmidataid** (14), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-215">Ob primärer VMQ-Prozessor aus der vrss-dereferenzierungstabelle ausgeschlossen werden soll, wenn vrss aktiviert ist. Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="8b42a-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-216">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8b42a-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-217">**Vrssindependenthostverteilung**</span><span class="sxs-lookup"><span data-stu-id="8b42a-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-218">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b42a-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-219">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-220">Qualifizierer: **wmidataid** (15), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-221">Gibt an, ob bei aktiviertem vrss immer Host seitiger vrss durchzuführen ist, unabhängig von der RSS-Einstellung der virtuellen NIC. Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="8b42a-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-222">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8b42a-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-223">**Vrssminqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="8b42a-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-224">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-225">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-226">Qualifizierer: **wmidataid** (12), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-227">Die Mindestanzahl von Warteschlangen, die bei Aktivierung von vrss zuzuordnen sind. Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8b42a-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-228">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8b42a-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-229">**Vrssqueueschedulingmode**</span><span class="sxs-lookup"><span data-stu-id="8b42a-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-231">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-232">Qualifizierer: **wmidataid** (13), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-233">Der zu verwendende Warteschlangen Planungsmodus, wenn vrss aktiviert ist. Der Standardwert ist die statische Zeitplanung.</span><span class="sxs-lookup"><span data-stu-id="8b42a-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-234">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8b42a-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b42a-235">**Vrssvmbuschannelaffinitypolicy**</span><span class="sxs-lookup"><span data-stu-id="8b42a-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b42a-236">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b42a-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-237">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b42a-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b42a-238">Qualifizierer: **wmidataid** (16), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8b42a-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8b42a-239">Die zu verwendende VMBus-channelaffinitäts Richtlinie, wenn vrss aktiviert ist. Der Standardwert ist "Strong".</span><span class="sxs-lookup"><span data-stu-id="8b42a-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="8b42a-240">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8b42a-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b42a-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b42a-241">Requirements</span></span>



| <span data-ttu-id="8b42a-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b42a-242">Requirement</span></span> | <span data-ttu-id="8b42a-243">Wert</span><span class="sxs-lookup"><span data-stu-id="8b42a-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b42a-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b42a-244">Minimum supported client</span></span><br/> | <span data-ttu-id="8b42a-245">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b42a-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b42a-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b42a-246">Minimum supported server</span></span><br/> | <span data-ttu-id="8b42a-247">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b42a-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b42a-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b42a-248">Namespace</span></span><br/>                | <span data-ttu-id="8b42a-249">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b42a-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b42a-250">MOF</span><span class="sxs-lookup"><span data-stu-id="8b42a-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b42a-251"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b42a-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b42a-252">DLL</span><span class="sxs-lookup"><span data-stu-id="8b42a-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b42a-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b42a-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

