---
description: Stellt die Replikations spezifischen Einstellungen für einen virtuellen Computer dar.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216576"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="1639a-103">MSVM \_ replicationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1639a-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="1639a-104">Stellt die Replikations spezifischen Einstellungen für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="1639a-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="1639a-105">Der Client übergibt eine Instanz dieser Klasse an [**MSVM \_ replicationservice. kreatereplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md) , um eine Replikations Beziehung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1639a-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="1639a-106">Der Client kann die Werte einer der Eigenschaften für diese Klasse nicht direkt ändern. Es muss die [**MSVM-Methode \_ replicationservice. modifyreplicationsettings**](modifyreplicationsettings-msvm-replicationservice.md) aufgerufen werden, um die Werte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1639a-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="1639a-107">Jede Replikations Beziehung verfügt über eine einzelne Instanz von Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1639a-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="1639a-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1639a-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1639a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1639a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="1639a-110">Member</span><span class="sxs-lookup"><span data-stu-id="1639a-110">Members</span></span>

<span data-ttu-id="1639a-111">Die **MSVM \_ replicationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1639a-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1639a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1639a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1639a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1639a-113">Properties</span></span>

<span data-ttu-id="1639a-114">Die **MSVM- \_ replicationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1639a-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1639a-115">**Additionalsettings**</span><span class="sxs-lookup"><span data-stu-id="1639a-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-118">Zusätzliche Replikationseinstellungen, die der Endpunkt Anbieter verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1639a-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="1639a-119">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1639a-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-120">**Applicationkonsistentsnapshotinterval**</span><span class="sxs-lookup"><span data-stu-id="1639a-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-121">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-123">Das Zeitintervall zwischen Anwendungs konsistenten Momentaufnahmen (angegeben in Stunden).</span><span class="sxs-lookup"><span data-stu-id="1639a-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="1639a-124">Gültige Werte liegen zwischen 1 Stunde und 12 Stunden.</span><span class="sxs-lookup"><span data-stu-id="1639a-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="1639a-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-128">Hiermit wird der Authentifizierungsmodus für die Verbindung mit dem Wiederherstellungs Server definiert.</span><span class="sxs-lookup"><span data-stu-id="1639a-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="1639a-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos-Authentifizierung** (1)</span><span class="sxs-lookup"><span data-stu-id="1639a-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1639a-130">Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1639a-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="1639a-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung** (2)</span><span class="sxs-lookup"><span data-stu-id="1639a-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1639a-132">Zertifikat basierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1639a-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1639a-133">**Automatikrecoveryaction**</span><span class="sxs-lookup"><span data-stu-id="1639a-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-136">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-136">Not used.</span></span>

<span data-ttu-id="1639a-137">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-138">**Automaticshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="1639a-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-141">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-141">Not used.</span></span>

<span data-ttu-id="1639a-142">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-143">**Automaticstartupaction**</span><span class="sxs-lookup"><span data-stu-id="1639a-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-146">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-146">Not used.</span></span>

<span data-ttu-id="1639a-147">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-148">**Automaticstartupactiondelay**</span><span class="sxs-lookup"><span data-stu-id="1639a-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-149">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1639a-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-151">Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1639a-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="1639a-152">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-153">**Automaticstartupactionsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="1639a-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-156">Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1639a-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="1639a-157">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-158">**Autoresynchronizeaktivierte**</span><span class="sxs-lookup"><span data-stu-id="1639a-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-159">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-161">Gibt an, ob Vorgänge zur erneuten Synchronisierung automatisch ausgelöst werden, wenn ein Replikations Fehler aufgrund von Strom-und Hardwarefehlern auftritt.</span><span class="sxs-lookup"><span data-stu-id="1639a-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="1639a-162">Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.</span><span class="sxs-lookup"><span data-stu-id="1639a-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="1639a-163">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1639a-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-164">**Autoresynchronizzutervalend**</span><span class="sxs-lookup"><span data-stu-id="1639a-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-165">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1639a-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-167">Gibt die Endzeit für die automatische Neusynchronisierung an, die ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="1639a-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="1639a-168">Dieser Wert ist Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="1639a-168">This value is in local time.</span></span> <span data-ttu-id="1639a-169">Der Standardwert ist 06:00 (6:00 Uhr).</span><span class="sxs-lookup"><span data-stu-id="1639a-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="1639a-170">Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.</span><span class="sxs-lookup"><span data-stu-id="1639a-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="1639a-171">Vorgänge zur erneuten Synchronisierung können auch geplant werden, damit Sie während des nächsten Intervalls ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-172">**Autoresynchronizeingetervalstart**</span><span class="sxs-lookup"><span data-stu-id="1639a-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-173">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1639a-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-175">Gibt die Startzeit für die automatische Neusynchronisierung an, die ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="1639a-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="1639a-176">Dieser Wert ist Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="1639a-176">This value is in local time.</span></span> <span data-ttu-id="1639a-177">Der Standardwert ist 18:30 (6:30 Uhr).</span><span class="sxs-lookup"><span data-stu-id="1639a-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="1639a-178">Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.</span><span class="sxs-lookup"><span data-stu-id="1639a-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="1639a-179">Vorgänge zur erneuten Synchronisierung können auch geplant werden, damit Sie während des nächsten Intervalls ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-180">**Bypassproxyserver**</span><span class="sxs-lookup"><span data-stu-id="1639a-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-181">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-183">Gibt an, ob der Proxy Server beim Herstellen einer Verbindung mit einem Wiederherstellungs Server umgangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1639a-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1639a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-187">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1639a-187">A short description of the object.</span></span> <span data-ttu-id="1639a-188">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikationseinstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1639a-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="1639a-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="1639a-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-193">Der Zertifikat Fingerabdruck, der verwendet werden soll, wenn die **AuthenticationType** -Eigenschaft eine Zertifikat basierte Authentifizierung ist.</span><span class="sxs-lookup"><span data-stu-id="1639a-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-194">**Compressionaktiviert**</span><span class="sxs-lookup"><span data-stu-id="1639a-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-195">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-197">Gibt an, ob Replikations Daten beim Senden an den Wiederherstellungs Server komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-198">**Configurationdataroot**</span><span class="sxs-lookup"><span data-stu-id="1639a-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-201">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-201">Not used.</span></span>

<span data-ttu-id="1639a-202">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-203">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="1639a-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-206">Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="1639a-207">Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1639a-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="1639a-208">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="1639a-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-212">Der eindeutige Bezeichner der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1639a-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="1639a-213">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="1639a-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-215">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1639a-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-217">Das Datum und die Uhrzeit der Erstellung der Einstellungen für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="1639a-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="1639a-218">Wenn dieses-Objekt die aktuellen Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der das System erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1639a-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="1639a-219">Wenn dieses-Objekt die Momentaufnahme Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der die Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1639a-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="1639a-220">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="1639a-221">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemsettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1639a-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="1639a-222">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-223">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1639a-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-226">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1639a-226">A description of the object.</span></span> <span data-ttu-id="1639a-227">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikations Einstellungsdaten für virtuelle Computer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="1639a-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1639a-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-231">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1639a-231">A display name for the object.</span></span> <span data-ttu-id="1639a-232">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und auf den anzeigen Amen für den virtuellen Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-233">**Enableschreiteorderkonservierungs ationacrossdisks**</span><span class="sxs-lookup"><span data-stu-id="1639a-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-234">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-236">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="1639a-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="1639a-237">Gibt an, ob alle replizierenden virtuellen Festplatten für die virtuelle Maschine auf denselben Zeitpunkt repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="1639a-238">Dadurch wird sichergestellt, dass die Replikation die Schreib Reihenfolge der Anwendungen auf dem virtuellen Computer berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1639a-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="1639a-239">**Windows 8.1:** Ab Windows 8.1 und Windows Server 2012 R2 ist diese Eigenschaft veraltet und wird immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-240">**Includdisks**</span><span class="sxs-lookup"><span data-stu-id="1639a-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-241">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1639a-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1639a-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-243">Qualifizierer: **hypervembeddedinstance** ("CIM \_ storagezucationsettingdata"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="1639a-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1639a-244">Die Liste der virtuellen Festplatten (VHDs), die mit dem System verbunden sind, das von der Replikations-Engine repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="1639a-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="1639a-245">Dabei handelt es sich um ein Array von Zeichen folgen, die jeweils die **InstanceId** der " [**MSVM \_ storagebereitungssettingdata**](msvm-storageallocationsettingdata.md) " enthalten, die die VHD darstellt.</span><span class="sxs-lookup"><span data-stu-id="1639a-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1639a-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-249">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1639a-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1639a-250">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1639a-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1639a-251">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="1639a-252">Für Windows 8 ist es immer auf "Microsoft:*Virtual Machine GUID* \\ HVR" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="1639a-253">Für Windows 8.1 ist die Einstellung "Microsoft:*GUID* \\ HVR \\<0/1>" für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1639a-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="1639a-254">Im Windows 8.1 Wert gibt 0 den primär Wert und 1 die erweiterte Replikation an.</span><span class="sxs-lookup"><span data-stu-id="1639a-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="1639a-255">Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="1639a-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-256">**Logdataroot**</span><span class="sxs-lookup"><span data-stu-id="1639a-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-259">Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="1639a-260">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-261">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="1639a-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-262">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1639a-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1639a-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-264">Nicht verwendet und kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-264">Not used and can't be set.</span></span>

<span data-ttu-id="1639a-265">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1639a-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-266">**Primaryconnectionpoint**</span><span class="sxs-lookup"><span data-stu-id="1639a-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-269">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1639a-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-270">Der Name des primären Verbindungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="1639a-270">The name of the primary connection point.</span></span> <span data-ttu-id="1639a-271">Bei einem primären Cluster ist dies der Name des Broker-Cap.</span><span class="sxs-lookup"><span data-stu-id="1639a-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="1639a-272">Bei einem eigenständigen primären Server handelt es sich hierbei um den Namen des Host Systems.</span><span class="sxs-lookup"><span data-stu-id="1639a-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-273">**Primaryhostsystem**</span><span class="sxs-lookup"><span data-stu-id="1639a-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-276">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1639a-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-277">Der voll qualifizierte Domänen Name des primären Host Systems, das den virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="1639a-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-278">**Wiederherstellungsconnectionpoint**</span><span class="sxs-lookup"><span data-stu-id="1639a-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-281">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1639a-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-282">Der Name des Wiederherstellungs Verbindungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="1639a-282">The name of the recovery connection point.</span></span> <span data-ttu-id="1639a-283">Bei einem Wiederherstellungs Cluster handelt es sich hierbei um den Broker-Cap-Namen.</span><span class="sxs-lookup"><span data-stu-id="1639a-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="1639a-284">Bei einem eigenständigen Wiederherstellungs Server handelt es sich hierbei um den Namen des Host Systems.</span><span class="sxs-lookup"><span data-stu-id="1639a-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-285">**Wiederherstellbare Datei**</span><span class="sxs-lookup"><span data-stu-id="1639a-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-288">Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="1639a-289">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-290">**Parameter recoveryhistory einen**</span><span class="sxs-lookup"><span data-stu-id="1639a-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-291">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-293">Die maximale Anzahl von Wiederherstellungs Momentaufnahmen, die auf dem Wiederherstellungs Server gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="1639a-294">Gültige Werte sind 0 bis 24.</span><span class="sxs-lookup"><span data-stu-id="1639a-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-295">**Wiederherstellunghostsystem**</span><span class="sxs-lookup"><span data-stu-id="1639a-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-298">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1639a-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-299">Der voll qualifizierte Domänen Name des Wiederherstellungs Host Systems, das den virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="1639a-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-300">**Wiederherstellserverportnummer**</span><span class="sxs-lookup"><span data-stu-id="1639a-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-301">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-303">Die Portnummer des Wiederherstellungs Servers, die beim Herstellen einer sicheren Verbindung für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1639a-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-304">**Replicatehostkvpitems**</span><span class="sxs-lookup"><span data-stu-id="1639a-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-305">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-307">Gibt an, ob nur Host- [**MSVM \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md)s vom primären virtuellen Computer auf den virtuellen Wiederherstellungs Computer repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1639a-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="1639a-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-309">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1639a-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-311">Replikations Intervall einer Replikations Beziehung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="1639a-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="1639a-312">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1639a-312">Valid values are:</span></span>

<span data-ttu-id="1639a-313">30</span><span class="sxs-lookup"><span data-stu-id="1639a-313">30</span></span>

<span data-ttu-id="1639a-314">300</span><span class="sxs-lookup"><span data-stu-id="1639a-314">300</span></span>

<span data-ttu-id="1639a-315">900</span><span class="sxs-lookup"><span data-stu-id="1639a-315">900</span></span>

<span data-ttu-id="1639a-316">Der Standardwert ist 300 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="1639a-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="1639a-317">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1639a-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-318">**Replicationprovider**</span><span class="sxs-lookup"><span data-stu-id="1639a-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-321">Der Pfad zur Instanz der [**MSVM- \_ replicationprovider**](msvm-replicationprovider.md) -Klasse, die den Endpunkt des Replikations Anbieters identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1639a-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="1639a-322">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1639a-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-323">**Rootcertifialisiethumschlag-Print**</span><span class="sxs-lookup"><span data-stu-id="1639a-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1639a-326">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="1639a-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="1639a-327">Der Fingerabdruck des Stamm Zertifikats des verwendeten Zertifikats, wenn " **AuthenticationType** " den Wert "2" hat (Zertifikat basierte Autorisierung).</span><span class="sxs-lookup"><span data-stu-id="1639a-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-328">**Snapshotdataroot**</span><span class="sxs-lookup"><span data-stu-id="1639a-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-331">Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="1639a-332">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-333">**Suspenddataroot**</span><span class="sxs-lookup"><span data-stu-id="1639a-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-336">Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="1639a-337">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-338">**Austauschen von Daten**</span><span class="sxs-lookup"><span data-stu-id="1639a-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-341">Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1639a-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="1639a-342">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1639a-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1639a-343">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="1639a-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-346">Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören.</span><span class="sxs-lookup"><span data-stu-id="1639a-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="1639a-347">Diese Eigenschaft ist eine außer Kraft Setzung von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1639a-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1639a-348">**Virtualsystemtype**</span><span class="sxs-lookup"><span data-stu-id="1639a-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1639a-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1639a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1639a-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1639a-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1639a-351">Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="1639a-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="1639a-352">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und ist immer auf "Microsoft: Hyper-V: Replica" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1639a-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1639a-353">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1639a-353">Requirements</span></span>



| <span data-ttu-id="1639a-354">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1639a-354">Requirement</span></span> | <span data-ttu-id="1639a-355">Wert</span><span class="sxs-lookup"><span data-stu-id="1639a-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1639a-356">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1639a-356">Minimum supported client</span></span><br/> | <span data-ttu-id="1639a-357">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1639a-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1639a-358">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1639a-358">Minimum supported server</span></span><br/> | <span data-ttu-id="1639a-359">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1639a-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1639a-360">Namespace</span><span class="sxs-lookup"><span data-stu-id="1639a-360">Namespace</span></span><br/>                | <span data-ttu-id="1639a-361">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1639a-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1639a-362">MOF</span><span class="sxs-lookup"><span data-stu-id="1639a-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1639a-363"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1639a-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1639a-364">DLL</span><span class="sxs-lookup"><span data-stu-id="1639a-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1639a-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1639a-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1639a-366">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1639a-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1639a-367">**CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="1639a-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="1639a-368">**Modifyreplicationsettings**</span><span class="sxs-lookup"><span data-stu-id="1639a-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

