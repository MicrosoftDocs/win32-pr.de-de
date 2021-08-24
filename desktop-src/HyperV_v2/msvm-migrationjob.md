---
description: Diese Klasse stellt einen Migrationsvorgangauftrag dar, der für die Speicher- oder Migration des virtuellen Systems durch den Migrationsdienst des virtuellen Systems erstellt wurde.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Msvm_MigrationJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba979953a9e7a17df70247cdb176cba2f5782d4f9f6fc13d8f4addc161bbaf50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521200"
---
# <a name="msvm_migrationjob-class"></a>Msvm \_ MigrationJob-Klasse

Diese Klasse stellt einen Migrationsvorgangauftrag dar, der für die Speicher- oder Migration des virtuellen Systems durch den Migrationsdienst des virtuellen Systems erstellt wurde.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ MigrationJob-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ MigrationJob-Klasse** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-migrationjob.md)                     | Ruft das Fehlerobjekt für den Migrationsauftrag ab, sofern vorhanden.<br/>                |
| [**GetErrorEx**](geterrorex-msvm-migrationjob.md)                 | Ruft die Fehlerobjekte für den Migrationsauftrag ab, sofern vorhanden.<br/>                |
| **KillJob**                                                        | Diese Methode wird nicht unterstützt.<br/>                                                   |
| [**RequestStateChange**](requeststatechange-msvm-migrationjob.md) | Fordert an, dass der Status des Migrationsauftrags in den angegebenen Zustand geändert wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MigrationJob-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Unkündbarem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag abgebrochen werden kann. Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag nach Abschluss automatisch gelöscht werden soll. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**DestinationHost**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Hostname der Zielvirtualisierungsplattform, zu der das virtuelle System migriert wird. Dies ist **null** für die Speichermigration.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** um zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall, in dem der Auftrag ausgeführt wurde, oder die Gesamtausführungszeit, wenn der Auftrag abgeschlossen ist. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein anbieterspezifischer Fehlercode. Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Herstellerfehlerbeschreibung enthält. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Auftrag**](cim-job.md).**ErrorCode**")
</dt> </dl>

Eine zusammenfassende Beschreibung des Fehlers( falls vorhanden).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionslos ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und immer auf 5 festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf **NULL festgelegt.**

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie oft der Auftrag ausgeführt werden soll. Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während jeder Wert ungleich 0 (null) ein Limit für die Anzahl der Wiederholungen des Auftrags angibt. 0 (null) gibt an, dass es keine Beschränkung für die Anzahl der Verarbeitungszeiten für den Auftrag gibt. Er wird jedoch entweder beendet, nachdem **UntilTime** erreicht wurde oder der Auftrag manuell beendet wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag geerbt.**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**JobState ist** eine ganzzahlige Enumeration, die den Betriebszustand eines Auftrags angibt. Sie kann auch Übergänge zwischen diesen Zuzuständen angeben, z. B. "Wird heruntergefahren" und "Wird gestartet". Diese Eigenschaft wird von [**CIM \_ ConcreteJob geerbt.**](/previous-versions//cc136808(v=vs.85))



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Neu**</dt> <dt>2</dt> </dl>                                                           | Der Auftrag wurde noch nie gestartet.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Ab**</dt> <dt>3</dt> </dl>                                       | Der Auftrag wird von den Status 2 (Neu), 5 (Angehalten) oder 11 (Dienst) in den Status 4 (Wird ausgeführt) überlaufen.<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Ausführung**</dt> <dt>von 4</dt> </dl>                                           | Der Auftrag wird ausgeführt.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Angehalten 5**</dt> <dt></dt> </dl>                                   | Der Auftrag wird beendet, kann aber nahtlos neu gestartet werden.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Herunterfahren 6**</dt> <dt></dt> </dl>                   | Der Auftrag wird in den Zustand 7 (Abgeschlossen), 8 (Beendet) oder 9 (Beendet) bewegt.<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Abgeschlossen**</dt> <dt>7</dt> </dl>                                   | Der Auftrag wurde normal abgeschlossen.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Beendet**</dt> <dt>8</dt> </dl>                               | Der Auftrag wurde durch eine Zustandsänderungsanforderung "Terminate" beendet. Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden. Die Anforderung, dass der Auftrag nur als neuer Auftrag neu gestartet wird, ist auftragsspezifisch.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**Killed**</dt> <dt>9</dt> </dl>                                               | Der Auftrag wurde durch eine Zustandsänderungsanforderung "Kill" beendet. Zugrunde liegende Prozesse werden möglicherweise noch ausgeführt, und möglicherweise ist eine Bereinigung erforderlich, um Ressourcen frei zu machen.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Ausnahme**</dt> <dt>10</dt> </dl>                                  | Der Auftrag befindet sich in einem nicht ungewöhnlichen Zustand, der auf einen Fehlerzustand hinde zeigt. Der tatsächliche Status des Auftrags kann über auftragsspezifische Objekte verfügbar sein.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Dienst**</dt> <dt>11</dt> </dl>                                          | Der Auftrag befindet sich in einem anbieterspezifischen Zustand, der die Problemermittlung, -lösung oder beides unterstützt.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>12 32767</dt> </dl>            | Reserviert.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt> </dl> | Reserviert.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**Auftragsstatus**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Auftragsstatus darstellt. Diese Eigenschaft wird vom [**\_ CIM-Auftrag geerbt.**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des Auftrags an, der von diesem Objekt nachverfolgt wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

**Erstellen eines virtuellen Remotecomputers** (300)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

**Überprüfen der Kompatibilität virtueller** Computer (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

**Überprüfen der Kompatibilität von virtuellen computern und Storage** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

**Überprüfen Storage Kompatibilität** (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

**Überprüfen Storage Migration** (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Verschieben eines virtuellen** Computers (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**Verschieben eines virtuellen Computers und Storage** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**Moving Storage** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird vom [**\_ CIM-Auftrag geerbt.**](/windows/desktop/CIMWin32Prov/cim-job)

Gibt an, ob die in den **Eigenschaften RunStartInterval und** **UntilTime** dargestellten Zeiten lokale Oder UTC-Zeiten darstellen.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2 )
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")
</dt> </dl>

Der von diesem Auftragsobjekt dargestellte Migrationstyp. Dies ist einer der Werte, die für die **MigrationType-Eigenschaft** der [**Msvm \_ VirtualSystemMigrationSettingData-Klasse definiert**](msvm-virtualsystemmigrationsettingdata.md) sind.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Der Anzeigename für diese Instanz eines Auftrags. Darüber hinaus kann der Anzeigename als Eigenschaft für eine Suche oder Abfrage verwendet werden. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**NewResourceSettingData**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einer Livemigration wird dies immer auf NULL **festgelegt.**

Wenn dies bei einer Speichermigration **NULL** ist, wird keine der virtuellen Festplatten (VHDs) des virtuellen Computers verschoben. Andernfalls enthält dies ein Array eingebetteter Instanzen der [**Msvm \_ StorageAllocationSettingData-Klasse,**](msvm-storageallocationsettingdata.md) die die zu verschobenen VHDs darstellen. Die **Connection-Eigenschaft** dieser Instanzen gibt den Zielspeicherort der VHD an.

</dd> <dt>

**NewSystemSettingData**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einer Livemigration wird dies immer auf NULL **festgelegt.**

Wenn dies bei einer Speichermigration **NULL ist,** werden die Datenswurzeln des virtuellen Computers nicht bewegt. Andernfalls enthält diese eine eingebettete Instanz der [**Msvm \_ VirtualSystemSettingData-Klasse,**](msvm-virtualsystemsettingdata.md) wobei die **Eigenschaften ExternalDataRoot,** **SnapshotDataRoot** und **SwapFileDataRoot** die neuen Datenswurzeln angeben.

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer, der bei Auftragsabschluss oder -fehler benachrichtigt wird. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements bereit und kann zum Bereitstellen weiterer Details in Bezug auf den Wert der **EnabledState-Eigenschaft** verwendet werden. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Wiederherstellungsaktion beschreibt, wenn die **RecoveryAction-Eigenschaft** der Instanz 1 (Sonstige) ist. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer, der den Auftrag übermittelt hat. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Einheiten** ( "Percent" )
</dt> </dl>

Der Abschlussprozentsatz des Auftrags. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um einen hohen und detaillierten Integritätsstatus des Elements und seiner Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Wichtigkeit der Ausführung eines Auftrags. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Wiederherstellungsaktion, die für einen nicht erfolgreich ausgeführten Auftrag ausgeführt werden soll. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortfahren** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Mit nächstem Auftrag fortfahren** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Wiederherstellungsauftrag ausführen** (5 )
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MinValue** ( -31 ), **MaxValue** ( 31 )
</dt> </dl>

Der Tag des Monats, an dem der Auftrag verarbeitet werden soll. Abhängig vom Wert von **RunDayOfWeek** gibt es unterschiedliche Interpretationen für diese Eigenschaft.

Wenn **RunDayOfWeek** 0 und **RunDay** positiv ist, definiert **RunDay** den Tag des Monats, an dem der Auftrag verarbeitet wird. Wenn **RunDayOfWeek** beispielsweise 0 und **RunDay** 12 ist, wird der Auftrag am 12. Tag des Monats verarbeitet.<sup></sup>

Wenn **RunDayOfWeek** 0 und **RunDay** negativ ist, definiert **RunDay** die Anzahl der Tage vor dem letzten Tag des Monats, an dem der Auftrag verarbeitet wird.  1 gibt den letzten Tag des Monats an, 2 gibt einen Tag vor dem letzten Tag des Monats an usw. Wenn **RunDayOfWeek** beispielsweise 0 und **RunDay** 1 ist, wird der Auftrag am letzten Tag des Monats verarbeitet.

Wenn **RunDayOfWeek** nicht 0 ist, ist **RunDayOfWeek** der Tag der Woche, an dem der Auftrag verarbeitet wird, relativ zu **RunDay**. Wenn **RunDay** beispielsweise 15 und **RunDayOfWeek** 7 (+Samstag) ist, wird der Auftrag am ersten Samstag am oder nach dem 15. Tag des Monats verarbeitet.<sup></sup> Wenn **RunDay** 20 und **RunDayOfWeek** 7 (Samstag) ist, wird der Auftrag am ersten Samstag am oder vor dem 20. Tag des Monats verarbeitet.<sup></sup> Wenn **RunDay** 1 und **RunDayOfWeek** 1 (Sonntag) ist, wird der Auftrag am letzten Sonntag des Monats verarbeitet.

Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine positive oder negative ganze Zahl, die in Verbindung mit **RunDay** verwendet wird, um den Tag der Woche oder des Monats anzugeben, an dem der Auftrag verarbeitet wird. Weitere Informationen finden Sie in der Beschreibung der **RunDay-Eigenschaft.** Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sonntag** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Montag** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Dienstag** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mittwoch** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Donnerstag** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Freitag** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samstag** (7 )
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Monat, in dem der Auftrag verarbeitet werden soll. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Januar** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Februar** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**März** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juni** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Juli** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Oktober** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezember** (11 )
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall nach Mitternacht, in dem der Auftrag verarbeitet werden soll. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die geplante Startzeit für den Auftrag, falls zutreffend. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit, zu der der Auftrag begonnen hat. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf "OK" festgelegt.

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeitspanne in Minuten, in der der Auftrag nach Abschluss der Ausführung beibehalten wird, entweder erfolgreich oder fehlgeschlagen. Der Auftrag muss unabhängig vom Wert der **DeleteOnCompletion-Eigenschaft** für einen bestimmten Zeitraum bestehen bleiben. Der Standardwert beträgt fünf Minuten. Diese Eigenschaft wird von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))geerbt und immer auf 000000000000500.000000:000 festgelegt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des Auftragszustands. Wenn sich der Status des Auftrags nicht geändert hat und diese Eigenschaft aufgefüllt wird, muss sie auf einen Intervallwert von 0 festgelegt werden. Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden. Diese Eigenschaft wird von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))geerbt.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit, zu der der Auftrag übermittelt wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag ungültig ist oder beendet werden soll. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name des betroffenen virtuellen Systems.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

