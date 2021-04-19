---
description: Stellt den Status der Switch-Hardware Auslagerung dar.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Msvm_EthernetSwitchHardwareOffloadData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367251"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="f6674-103">MSVM \_ ethernezwitchhardwareoffloaddata-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6674-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="f6674-104">Stellt den Status der Switch-Hardware Auslagerung dar.</span><span class="sxs-lookup"><span data-stu-id="f6674-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="f6674-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6674-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6674-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6674-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="f6674-107">Member</span><span class="sxs-lookup"><span data-stu-id="f6674-107">Members</span></span>

<span data-ttu-id="f6674-108">Die **MSVM \_ ethernezwitchhardwareoffloaddata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f6674-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="f6674-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6674-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6674-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6674-110">Properties</span></span>

<span data-ttu-id="f6674-111">Die **MSVM \_ ethernezwitchhardwareoffloaddata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6674-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6674-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f6674-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6674-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6674-115">A short description of the object.</span></span> <span data-ttu-id="f6674-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-117">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f6674-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-120">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6674-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-121">Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6674-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="f6674-122">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-123">**Defaultqueuevmmqaktivierte**</span><span class="sxs-lookup"><span data-stu-id="f6674-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-126">Qualifizierer: **wmidataid** (11), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-127">Die aktuelle vmmq-Einstellung für die Standard Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f6674-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="f6674-128">Die Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6674-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-129">**Defaultqueuevmmqqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="f6674-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-132">Qualifizierer: **wmidataid** (12), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-133">Die aktuelle Anzahl der der Standard Warteschlange zugeordneten Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="f6674-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="f6674-134">Die Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6674-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-135">**Defaultqueuevrssaktivierte**</span><span class="sxs-lookup"><span data-stu-id="f6674-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-138">Qualifizierer: **wmidataid** (10), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-139">Die aktuelle vrss-Einstellung für die Standard Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f6674-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="f6674-140">Die Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6674-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-141">**Defaultqueuevrssexcludeprimaryprocessor**</span><span class="sxs-lookup"><span data-stu-id="f6674-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-144">Qualifizierer: **wmidataid** (15), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-145">Gibt an, ob die primäre VMQ-CPU von der vrss/vmmq-dereferenzierungstabelle ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f6674-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="f6674-146">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="f6674-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-147">**Defaultqueuevrssindependenthostverteilung**</span><span class="sxs-lookup"><span data-stu-id="f6674-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-150">Qualifizierer: **wmidataid** (16), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-151">Gibt an, ob die vrss-Verteilung für die Standard Warteschlange unabhängig vom RSS-Status des externen VPORTS immer durchzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="f6674-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="f6674-152">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="f6674-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-153">**Defaultqueuevrssminqueuepairs**</span><span class="sxs-lookup"><span data-stu-id="f6674-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-156">Qualifizierer: **wmidataid** (13), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-157">Gibt die Mindestanzahl von Warteschlangen an, die für vrss/vmmq verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="f6674-158">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="f6674-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-159">**Defaultqueuevrssqueueschedulingmode**</span><span class="sxs-lookup"><span data-stu-id="f6674-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-162">Qualifizierer: **wmidataid** (14), **interfacetten** (4), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-163">Gibt an, wie vrss/vmmq-Warteschlangen an verschiedene Host Prozessoren geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="f6674-164">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="f6674-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-165">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6674-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6674-168">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6674-168">A description of the object.</span></span> <span data-ttu-id="f6674-169">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6674-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6674-173">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6674-173">A display name for the object.</span></span> <span data-ttu-id="f6674-174">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6674-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-178">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f6674-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6674-179">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f6674-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6674-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-181">**Iovqueuepairren Capacity**</span><span class="sxs-lookup"><span data-stu-id="f6674-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-184">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-185">Die maximale Anzahl von Warteschlangen Paaren, die vom Schalter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-186">**Iovqueuepairusage**</span><span class="sxs-lookup"><span data-stu-id="f6674-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-189">Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-190">Die aktuelle Anzahl der Warteschlangen Paare, die vom Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-191">**Iovvfcapacity**</span><span class="sxs-lookup"><span data-stu-id="f6674-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-192">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-194">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-195">Die maximale Anzahl von virtuellen Funktionen, die vom Schalter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-196">**Iovvfusage**</span><span class="sxs-lookup"><span data-stu-id="f6674-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-199">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-200">Die aktuelle Anzahl von virtuellen Funktionen, die vom Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-201">**Ipsecsacapacity**</span><span class="sxs-lookup"><span data-stu-id="f6674-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-202">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-204">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-205">Die maximale Anzahl von IPSec-Sicherheits Zuordnungs Abladungen, die vom Switch unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-206">**Ipsecwurst**</span><span class="sxs-lookup"><span data-stu-id="f6674-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-209">Qualifizierer: **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-210">Die aktuelle Anzahl von IPSec-Sicherheits Zuordnungs Abladungen, die vom Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-211">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6674-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-214">Qualifizierer: **Key**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6674-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-215">Der eindeutige Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f6674-215">The unique name of the resource.</span></span> <span data-ttu-id="f6674-216">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-217">**Packetdirectinuse**</span><span class="sxs-lookup"><span data-stu-id="f6674-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-218">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-220">Qualifizierer: **wmidataid** (9), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-221">Gibt an, ob Paket Direct vom Switch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6674-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="f6674-222">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6674-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f6674-223">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f6674-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-226">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6674-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-227">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="f6674-227">The hosting system's creation class name.</span></span> <span data-ttu-id="f6674-228">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-229">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f6674-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6674-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-232">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6674-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-233">Der Name des virtuellen Switchs, an den die zugeordnete Ressourcen Instanz gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f6674-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="f6674-234">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6674-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6674-235">**Vmqcapacity**</span><span class="sxs-lookup"><span data-stu-id="f6674-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-236">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-238">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-239">Die maximale Anzahl von Warteschlangen Abladungen virtueller Computer, die vom Switch unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f6674-240">**Vmqusage**</span><span class="sxs-lookup"><span data-stu-id="f6674-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6674-241">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6674-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6674-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6674-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6674-243">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f6674-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f6674-244">Die aktuelle Anzahl der Warteschlangen Abladungen des virtuellen Computers, die vom Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6674-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6674-245">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6674-245">Requirements</span></span>



| <span data-ttu-id="f6674-246">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6674-246">Requirement</span></span> | <span data-ttu-id="f6674-247">Wert</span><span class="sxs-lookup"><span data-stu-id="f6674-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6674-248">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6674-248">Minimum supported client</span></span><br/> | <span data-ttu-id="f6674-249">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6674-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6674-250">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6674-250">Minimum supported server</span></span><br/> | <span data-ttu-id="f6674-251">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6674-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6674-252">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6674-252">Namespace</span></span><br/>                | <span data-ttu-id="f6674-253">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f6674-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6674-254">MOF</span><span class="sxs-lookup"><span data-stu-id="f6674-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6674-255"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6674-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6674-256">DLL</span><span class="sxs-lookup"><span data-stu-id="f6674-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6674-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6674-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

