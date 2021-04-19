---
description: Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften. CIM \_ virtualsystemsettingdata wird auch als Klasse der obersten Ebene der virtuellen Systemkonfigurationen verwendet.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368921"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="218d2-104">CIM \_ virtualsystemsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="218d2-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="218d2-105">Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="218d2-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="218d2-106">**CIM \_ Virtualsystemsettingdata** wird auch als Klasse der obersten Ebene der virtuellen Systemkonfigurationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="218d2-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="218d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="218d2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
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
};
```

## <a name="members"></a><span data-ttu-id="218d2-108">Member</span><span class="sxs-lookup"><span data-stu-id="218d2-108">Members</span></span>

<span data-ttu-id="218d2-109">Die **CIM- \_ virtualsystemsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="218d2-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="218d2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="218d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="218d2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="218d2-111">Properties</span></span>

<span data-ttu-id="218d2-112">Die **CIM- \_ virtualsystemsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="218d2-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="218d2-113">**Automatikrecoveryaction**</span><span class="sxs-lookup"><span data-stu-id="218d2-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="218d2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-116">Die für das virtuelle System auszuführende Aktion, wenn die vom virtuellen System ausgeführte Software ausfällt.</span><span class="sxs-lookup"><span data-stu-id="218d2-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="218d2-117">Zu den von dieser Eigenschaft behandelten Fehlern zählen nur solche, die von der Host Plattform erkannt werden, z. b. eine nicht unter brechbare Bedingung für den Wartezustand.</span><span class="sxs-lookup"><span data-stu-id="218d2-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="218d2-118">**Keine** (2)</span><span class="sxs-lookup"><span data-stu-id="218d2-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="218d2-119">**Neu starten** (3)</span><span class="sxs-lookup"><span data-stu-id="218d2-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="218d2-120">**Momentaufnahme** wiederherstellen (4)</span><span class="sxs-lookup"><span data-stu-id="218d2-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="218d2-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="218d2-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="218d2-122">**Automaticshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="218d2-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="218d2-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-125">Die Aktion, die beim Herunterfahren des Hosts für das virtuelle System ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="218d2-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="218d2-126">**Ausschalten** (2)</span><span class="sxs-lookup"><span data-stu-id="218d2-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="218d2-127">**Zustand speichern** (3)</span><span class="sxs-lookup"><span data-stu-id="218d2-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="218d2-128">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="218d2-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="218d2-129">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="218d2-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="218d2-130">**Automaticstartupaction**</span><span class="sxs-lookup"><span data-stu-id="218d2-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="218d2-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-133">Die Aktion, die beim Starten des Hosts auf dem virtuellen System ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="218d2-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="218d2-134">**Keine** (2)</span><span class="sxs-lookup"><span data-stu-id="218d2-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="218d2-135">**Neu starten, wenn zuvor aktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="218d2-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="218d2-136">**Immer starten** (4)</span><span class="sxs-lookup"><span data-stu-id="218d2-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="218d2-137">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="218d2-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="218d2-138">**Automaticstartupactiondelay**</span><span class="sxs-lookup"><span data-stu-id="218d2-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-139">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="218d2-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-141">Die Verzögerung für die Start Aktion.</span><span class="sxs-lookup"><span data-stu-id="218d2-141">The delay for the startup action.</span></span> <span data-ttu-id="218d2-142">Dieser Wert ist eine Intervall Variante des **DateTime** -Datentyps.</span><span class="sxs-lookup"><span data-stu-id="218d2-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-143">**Automaticstartupactionsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="218d2-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="218d2-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-146">Die Sequenznummer für die Aktivierung des virtuellen Systems, wenn das Host System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="218d2-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="218d2-147">Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin.</span><span class="sxs-lookup"><span data-stu-id="218d2-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="218d2-148">Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="218d2-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="218d2-149">Der Wert "0" gibt an, dass die Sequenz implementierungsabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="218d2-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-150">**Configurationdataroot**</span><span class="sxs-lookup"><span data-stu-id="218d2-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-153">Der Dateipfad des Verzeichnisses, in dem Informationen zur Konfiguration des virtuellen Systems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="218d2-154">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-155">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="218d2-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-158">Der relative Pfad der Datei, in der Informationen über die Konfiguration des virtuellen Systems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="218d2-159">Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="218d2-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="218d2-160">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="218d2-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-164">Die eindeutige ID der virtuellen Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="218d2-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="218d2-165">**Configurationid** unterscheidet sich von der **InstanceId** und wird von der Implementierung einem virtuellen System oder einer virtuellen Systemkonfiguration zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="218d2-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="218d2-166">**Configurationid** ist kein Schlüssel, und der gleiche Wert kann für mehr als eine Instanz auftreten.</span><span class="sxs-lookup"><span data-stu-id="218d2-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="218d2-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="218d2-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-168">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="218d2-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-170">Das Datum und die Uhrzeit der Erstellung der virtuellen Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="218d2-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-171">**Logdataroot**</span><span class="sxs-lookup"><span data-stu-id="218d2-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-174">Der relative Dateipfad des Verzeichnisses, in dem die Protokollinformationen für das virtuelle System gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="218d2-175">Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="218d2-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="218d2-176">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-177">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="218d2-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-178">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="218d2-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="218d2-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-180">Ein Array, das vom Benutzer bereitgestellte Notizen enthält, die mit dem virtuellen System verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="218d2-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-181">**Wiederherstellbare Datei**</span><span class="sxs-lookup"><span data-stu-id="218d2-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-184">Der Pfad der Datei, in der Wiederherstellungs bezogene Informationen des virtuellen Systems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="218d2-185">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-186">**Snapshotdataroot**</span><span class="sxs-lookup"><span data-stu-id="218d2-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-189">Der relative Pfad des Verzeichnisses, in dem Informationen zu virtuellen System Momentaufnahmen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="218d2-190">Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="218d2-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="218d2-191">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-192">**Suspenddataroot**</span><span class="sxs-lookup"><span data-stu-id="218d2-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-195">Der relative Pfad des Verzeichnisses, in dem die zusammenhängenden Informationen zum virtuellen System gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="218d2-196">Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="218d2-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="218d2-197">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-198">**Austauschen von Daten**</span><span class="sxs-lookup"><span data-stu-id="218d2-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-201">Der relative Dateipfad des Verzeichnisses, in dem die Auslagerungs Dateien des virtuellen Systems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="218d2-202">Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="218d2-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="218d2-203">Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-204">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="218d2-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-207">Der eindeutige Name für das System innerhalb der Virtualisierungsplattform.</span><span class="sxs-lookup"><span data-stu-id="218d2-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="218d2-208">**Virtualsystemtifier** ist nicht der Hostname, der der im virtuellen System laufenden Betriebssystem Instanz zugewiesen ist, oder es handelt sich um eine IP-Adresse oder Mac-Adresse, die einem der zugehörigen Netzwerkports zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="218d2-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="218d2-209">Der **virtualsystemtifier** kann Implementierungs spezifische Regeln enthalten, z. b. einfache Muster oder einen regulären Ausdruck, der von der Implementierung beim Festlegen von **virtualsystemdentifier** interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="218d2-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="218d2-210">**Virtualsystemtype**</span><span class="sxs-lookup"><span data-stu-id="218d2-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="218d2-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="218d2-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="218d2-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="218d2-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="218d2-213">Der Typ des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="218d2-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="218d2-214">Wenn der Typ des virtuellen Systems unbekannt ist, muss dieser Wert auf "DMTF: Unknown" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="218d2-215">Diese Eigenschaft wird mit dem folgenden Format der erweiterten Backus-Naur Form (ABNF) formatiert:</span><span class="sxs-lookup"><span data-stu-id="218d2-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="218d2-216">vs-Type = DMTF-Value/other-org-Value/Legacy-Value; DMTF-Value = "DMTF:" definierende-org ":" org-vs-Type; Other-org-value = Definition-org ":" org-vs-Type;</span><span class="sxs-lookup"><span data-stu-id="218d2-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="218d2-217">Der Wert des obigen ABNF-Formats lautet:</span><span class="sxs-lookup"><span data-stu-id="218d2-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="218d2-218">*DMTF: Wert*   ein durch DMTF definierter Eigenschafts Wert, der in der Beschreibung dieser Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="218d2-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="218d2-219">*other-org-Value*   ist ein Eigenschafts Wert, der von einer anderen Geschäfts Entität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="218d2-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="218d2-220">*Legacy-Wert*   ein Eigenschafts Wert, der von einer anderen Geschäfts Entität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="218d2-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="218d2-221">Diese Werte sind zulässig, werden jedoch im Laufe der Zeit als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="218d2-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="218d2-222">*Definieren von-org ein Bezeichner*   für die Geschäfts Entität, die den virtuellen Systemtyp definiert.</span><span class="sxs-lookup"><span data-stu-id="218d2-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="218d2-223">Er sollte ein urheberrechtlich geschütztes, mit einem oder einen mit einem Wert bezeichnetes oder einen eindeutigen Namen enthalten, der im Besitz der Geschäfts Entität</span><span class="sxs-lookup"><span data-stu-id="218d2-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="218d2-224">Er darf nicht "DMTF" lauten und darf keinen Doppelpunkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="218d2-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="218d2-225">*org-vs-geben Sie einen Bezeichner*   für den virtuellen Systemtyp innerhalb der definierenden Geschäfts Entität ein.</span><span class="sxs-lookup"><span data-stu-id="218d2-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="218d2-226">Er sollte innerhalb von Definition-org eindeutig sein. "org-vs-Type" kann beliebige Zeichen verwenden, die für CIM-Zeichen folgen zulässig sind, mit Ausnahme der folgenden: U0000-U001F (Unicode-Steuerelemente), U0020 (Leerzeichen), U007F (Unicode-Steuerelemente) oder U0080-U009F (Unicode C1-Steuerelemente).</span><span class="sxs-lookup"><span data-stu-id="218d2-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="218d2-227">Wenn der Wert in Segmente strukturiert werden muss, sollten die Segmente durch einen einzelnen Doppelpunkt getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="218d2-228">Die Werte dieser Eigenschaft sollten in der Groß-/Kleinschreibung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="218d2-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="218d2-229">Sie sollen nicht als Anzeige Name, sondern Programm gesteuert verarbeitet werden, und es sollte kurz sein.</span><span class="sxs-lookup"><span data-stu-id="218d2-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="218d2-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="218d2-230">Requirements</span></span>



| <span data-ttu-id="218d2-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="218d2-231">Requirement</span></span> | <span data-ttu-id="218d2-232">Wert</span><span class="sxs-lookup"><span data-stu-id="218d2-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="218d2-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="218d2-233">Minimum supported client</span></span><br/> | <span data-ttu-id="218d2-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="218d2-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="218d2-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="218d2-235">Minimum supported server</span></span><br/> | <span data-ttu-id="218d2-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="218d2-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="218d2-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="218d2-237">Namespace</span></span><br/>                | <span data-ttu-id="218d2-238">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="218d2-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="218d2-239">MOF</span><span class="sxs-lookup"><span data-stu-id="218d2-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="218d2-240"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="218d2-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="218d2-241">DLL</span><span class="sxs-lookup"><span data-stu-id="218d2-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="218d2-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="218d2-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="218d2-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="218d2-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218d2-244">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="218d2-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




