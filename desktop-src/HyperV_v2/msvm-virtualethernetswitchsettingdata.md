---
description: Stellt die aktuelle Konfiguration eines virtuellen Ethernet-Switchs dar.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359991"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="3a657-103">MSVM \_ virtualethernetzwitchsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="3a657-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="3a657-104">Stellt die aktuelle Konfiguration eines virtuellen Ethernet-Switchs dar.</span><span class="sxs-lookup"><span data-stu-id="3a657-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="3a657-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a657-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a657-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a657-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="3a657-107">Member</span><span class="sxs-lookup"><span data-stu-id="3a657-107">Members</span></span>

<span data-ttu-id="3a657-108">Die **MSVM \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3a657-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3a657-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a657-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a657-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a657-110">Properties</span></span>

<span data-ttu-id="3a657-111">Die **MSVM \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a657-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a657-112">**Associatedresourcepool**</span><span class="sxs-lookup"><span data-stu-id="3a657-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3a657-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a657-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-115">Eine Liste der Host Ressourcenpools, die zugeordnet werden müssen oder die derzeit dem Ethernet-Switch zum Zweck der Zuordnung von Ethernet-Verbindungen zwischen einem virtuellen Computer und einem Ethernet-Switch zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3a657-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="3a657-116">Jeder Wert muss dem in DSP0207 definierten produktionswbem- \_ URI \_ untypedinstancepath entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3a657-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="3a657-117">Diese Eigenschaft wird von **CIM \_ virtualethernettwitchsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-118">**Automatikrecoveryaction**</span><span class="sxs-lookup"><span data-stu-id="3a657-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a657-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-121">Die für den virtuellen Computer auszuführende Aktion, wenn die von der virtuellen Maschine ausgeführte Software ausfällt.</span><span class="sxs-lookup"><span data-stu-id="3a657-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="3a657-122">Fehler sind in diesem Fall ein Fehler, der von der Host Plattform erkannt werden kann, z. b. eine nicht unter brechbare Bedingung für den Wartezustand.</span><span class="sxs-lookup"><span data-stu-id="3a657-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="3a657-123">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-124">**Automaticshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="3a657-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a657-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-127">Aktion, die beim Herunterfahren des Hosts für die virtuelle Maschine ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a657-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="3a657-128">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-129">**Automaticstartupaction**</span><span class="sxs-lookup"><span data-stu-id="3a657-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a657-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-132">Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3a657-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="3a657-133">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-134">**Automaticstartupactiondelay**</span><span class="sxs-lookup"><span data-stu-id="3a657-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a657-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-137">Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3a657-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="3a657-138">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-139">**Automaticstartupactionsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="3a657-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a657-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-142">Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3a657-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="3a657-143">Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin.</span><span class="sxs-lookup"><span data-stu-id="3a657-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="3a657-144">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-145">**Bandwidthreservationmode**</span><span class="sxs-lookup"><span data-stu-id="3a657-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a657-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a657-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a657-148">Der Bandbreiten Reservierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="3a657-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="3a657-149">**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="3a657-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="3a657-150">**Gewichtung** (1)</span><span class="sxs-lookup"><span data-stu-id="3a657-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="3a657-151">**Absolut** (2)</span><span class="sxs-lookup"><span data-stu-id="3a657-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3a657-152">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="3a657-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a657-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a657-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-156">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a657-156">A short description of the object.</span></span> <span data-ttu-id="3a657-157">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für virtuelle Ethernet-Switches" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a657-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3a657-158">**Configurationdataroot**</span><span class="sxs-lookup"><span data-stu-id="3a657-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-161">Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3a657-162">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-163">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="3a657-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-166">Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3a657-167">Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3a657-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3a657-168">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="3a657-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-172">Der eindeutige Bezeichner der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="3a657-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="3a657-173">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="3a657-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-175">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a657-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-177">Das Datum und die Uhrzeit der Erstellung der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="3a657-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="3a657-178">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a657-179">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a657-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-182">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a657-182">A description of the object.</span></span> <span data-ttu-id="3a657-183">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "aktive Einstellungen für den virtuellen Ethernet-Switch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a657-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="3a657-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a657-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-187">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a657-187">A display name for the object.</span></span> <span data-ttu-id="3a657-188">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a657-189">**Extensionorder**</span><span class="sxs-lookup"><span data-stu-id="3a657-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-190">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3a657-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a657-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a657-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a657-192">Ein Array von eingebetteten Instanzen der [**MSVM-Klasse " \_ ethernetzwitchextension**](msvm-ethernetswitchextension.md) ", die die an diesen Switch gebundenen switcherweiterungen in der Reihenfolge darstellt, in der Sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a657-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a657-196">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="3a657-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a657-197">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="3a657-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a657-198">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) geerbt und ist immer auf "Microsoft:*GUID* Geräte-ID- \\ *Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a657-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="3a657-199">**Iovbevorzugt**</span><span class="sxs-lookup"><span data-stu-id="3a657-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-200">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a657-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-201">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a657-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a657-202">Gibt an, ob eine Single-root-e/a-Virtualisierung (SR-IOV) auf dem zugrunde liegenden Adapter bevorzugt oder nicht, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a657-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-203">**Logdataroot**</span><span class="sxs-lookup"><span data-stu-id="3a657-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-206">Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="3a657-207">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-208">**Maxnummacaddress**</span><span class="sxs-lookup"><span data-stu-id="3a657-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-209">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a657-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-211">Gibt die maximale Anzahl von eindeutigen MAC-Adressen an, die vom Switch zur Unterstützung von Mac-Adressen, wie im IEEE 802,1-Standard definiert, erlernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a657-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="3a657-212">Diese Eigenschaft wird von **CIM \_ virtualethernettwitchsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-213">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="3a657-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-214">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3a657-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a657-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-216">Vom Benutzer bereitgestellte Hinweise zum virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3a657-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="3a657-217">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a657-218">**Packetdirectenabled**</span><span class="sxs-lookup"><span data-stu-id="3a657-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a657-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a657-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a657-221">Gibt an, ob "packetdirect" verwendet werden soll, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a657-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="3a657-222">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="3a657-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="3a657-223">Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3a657-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a657-224">**Wiederherstellbare Datei**</span><span class="sxs-lookup"><span data-stu-id="3a657-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-227">Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="3a657-228">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-229">**Snapshotdataroot**</span><span class="sxs-lookup"><span data-stu-id="3a657-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-232">Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="3a657-233">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-234">**Suspenddataroot**</span><span class="sxs-lookup"><span data-stu-id="3a657-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-237">Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="3a657-238">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-239">**Austauschen von Daten**</span><span class="sxs-lookup"><span data-stu-id="3a657-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-242">Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a657-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="3a657-243">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a657-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a657-244">**Teamingenabled**</span><span class="sxs-lookup"><span data-stu-id="3a657-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a657-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-246">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3a657-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a657-247">Gibt an, ob NIC-Teaming verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a657-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="3a657-248">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="3a657-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="3a657-249">Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3a657-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a657-250">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="3a657-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-253">Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören.</span><span class="sxs-lookup"><span data-stu-id="3a657-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="3a657-254">Diese Eigenschaft ist eine außer Kraft Setzung von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a657-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a657-255">**Virtualsystemtype**</span><span class="sxs-lookup"><span data-stu-id="3a657-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a657-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a657-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-258">Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="3a657-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="3a657-259">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a657-260">**Vlanconnection**</span><span class="sxs-lookup"><span data-stu-id="3a657-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a657-261">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3a657-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a657-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a657-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a657-263">Eine Liste von VLAN-Bezeichner, auf die dieser Switch zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3a657-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="3a657-264">Diese Eigenschaft wird von **CIM \_ virtualethernettwitchsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a657-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a657-265">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a657-265">Requirements</span></span>



| <span data-ttu-id="3a657-266">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a657-266">Requirement</span></span> | <span data-ttu-id="3a657-267">Wert</span><span class="sxs-lookup"><span data-stu-id="3a657-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a657-268">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a657-268">Minimum supported client</span></span><br/> | <span data-ttu-id="3a657-269">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a657-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a657-270">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a657-270">Minimum supported server</span></span><br/> | <span data-ttu-id="3a657-271">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a657-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a657-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a657-272">Namespace</span></span><br/>                | <span data-ttu-id="3a657-273">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a657-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a657-274">MOF</span><span class="sxs-lookup"><span data-stu-id="3a657-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a657-275"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a657-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a657-276">DLL</span><span class="sxs-lookup"><span data-stu-id="3a657-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a657-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a657-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

