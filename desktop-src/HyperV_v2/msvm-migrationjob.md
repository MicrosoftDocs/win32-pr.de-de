---
description: Diese Klasse stellt einen Migrations Vorgangs Auftrag dar, der für die Migration des virtuellen System Migrations Dienstanbieter oder des virtuellen Systems erstellt wurde.
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
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372963"
---
# <a name="msvm_migrationjob-class"></a>MSVM \_ migrationjob-Klasse

Diese Klasse stellt einen Migrations Vorgangs Auftrag dar, der für die Migration des virtuellen System Migrations Dienstanbieter oder des virtuellen Systems erstellt wurde.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ migrationjob** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ migrationjob** -Klasse verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-migrationjob.md)                     | Ruft das Fehler Objekt für den Migrations Auftrag ab, sofern vorhanden.<br/>                |
| [**Geterrorex**](geterrorex-msvm-migrationjob.md)                 | Ruft die Fehler Objekte für den Migrations Auftrag ab, sofern vorhanden.<br/>                |
| **Killjob**                                                        | Diese Methode wird nicht unterstützt.<br/>                                                   |
| [**RequestStateChange**](requeststatechange-msvm-migrationjob.md) | Fordert an, dass der Status des Migrations Auftrags in den angegebenen Zustand geändert wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ migrationjob** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Abbrechbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag abgebrochen werden kann. Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Deleteoncompletion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag nach Abschluss des Vorgangs automatisch gelöscht werden soll. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Destinationhost**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Hostname der zielvirtualisierungsplattform, zu der das virtuelle System migriert wird. Dieser Wert wird für die Speicher Migration **null** sein.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Verweilzeit**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall, in dem der Auftrag ausgeführt wurde, oder die Gesamt Ausführungszeit, wenn der Auftrag abgeschlossen ist. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Hersteller spezifischer Fehlercode. Der Wert muss auf 0 (null) festgelegt werden, wenn der Auftrag ohne Fehler abgeschlossen wurde. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Hersteller Fehlerbeschreibung enthält. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")
</dt> </dl>

Eine zusammenfassende Beschreibung des Fehlers, falls vorhanden.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten. Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Jobruntimes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie oft der Auftrag ausgeführt werden soll. Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während ein Wert ungleich NULL einen Grenzwert für die Häufigkeit angibt, mit der der Auftrag wiederholt wird. NULL gibt an, dass es keine Beschränkung gibt, wie oft der Auftrag verarbeitet werden kann. er wird jedoch entweder beendet, nachdem die **untilzeit** erreicht wurde, oder der Auftrag wird manuell beendet. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**Jobstate** ist eine ganzzahlige Enumeration, die den Betriebszustand eines Auftrags angibt. Sie kann auch die Übergänge zwischen diesen Zuständen angeben, z. b. "Herunterfahren" und "starten". Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Neu**</dt> <dt>2</dt> </dl>                                                           | Der Auftrag wurde nie gestartet.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Ab**</dt> <dt>3</dt> </dl>                                       | Der Auftrag wechselt von den Zuständen 2 (neu), 5 (angehalten) oder 11 (Dienst) in den Zustand 4 (wird ausgeführt).<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Ausführen**</dt> von <dt>4</dt> </dl>                                           | Der Auftrag wird ausgeführt.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt></dt> Angehalten <dt>5</dt> </dl>                                   | Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Herunter**</dt> fahren <dt>6</dt> </dl>                   | Der Auftrag wechselt in den Status 7 (abgeschlossen), 8 (beendet) oder 9 (abgebrochen).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Abgeschlossen**</dt> <dt>7</dt> </dl>                                   | Der Auftrag wurde normal abgeschlossen.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Beendet**</dt> <dt>8</dt> </dl>                               | Der Auftrag wurde mit dem Status "beenden" beendet Change Request. Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden. Die Anforderung, dass der Auftrag nur dann neu gestartet werden soll, wenn ein neuer Auftrag ein Auftrags spezifischer Auftrag ist.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt></dt> <dt>9</dt> abgebrochen </dl>                                               | Der Auftrag wurde mit dem Status "Kill" beendet Change Request. Zugrunde liegende Prozesse können weiterhin ausgeführt werden, und es ist möglicherweise ein Cleanup erforderlich, um Ressourcen freizugeben.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Ausnahme**</dt> <dt>10</dt> </dl>                                  | Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist. Der tatsächliche Status des Auftrags ist möglicherweise über auftragsspezifische Objekte verfügbar.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Dienst**</dt> <dt>11</dt> </dl>                                          | Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung oder-Lösung oder beides unterstützt.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>12 32767</dt> </dl>            | Reserviert.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt> </dl> | Reserviert.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**Auftragsstatus**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Auftragsstatus darstellt. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des Auftrags an, der von diesem-Objekt nachverfolgt wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

Der **virtuelle Remote Computer wird erstellt** (300).


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

Über **Prüfen der Kompatibilität der virtuellen Maschine** (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

Über **Prüfen der Kompatibilität virtueller Computer und Speicher** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

Über **Prüfen der Speicher Kompatibilität** (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

Über **Prüfen der Speicher Migration** (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Verschieben des virtuellen** Computers (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**Verschieben von virtuellen Maschinen und Speicher** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**Verschieben von Speicher** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**Localorutctime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

Gibt an, ob die in den Eigenschaften **runstartinterval** und **UntilTime** dargestellten Uhrzeiten Ortszeit oder UTC-Zeiten darstellen.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2)
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md)".**MigrationType**")
</dt> </dl>

Der durch dieses Auftrags Objekt dargestellte Migrationstyp. Dies ist einer der Werte, die für die **migrationType** -Eigenschaft der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse definiert werden.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Anzeige Name für diese Instanz eines Auftrags. Außerdem kann der Anzeige Name als Eigenschaft für eine Suche oder Abfrage verwendet werden. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Newresourcesettingdata**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einer Live Migration wird dies immer auf **null** festgelegt.

Bei einer Speicher Migration werden die virtuellen Festplatten (VHDs) der virtuellen Maschine verschoben, wenn diese **null** ist. Andernfalls enthält dies ein Array von eingebetteten Instanzen der Klasse " [**MSVM \_ storagezudationsettingdata**](msvm-storageallocationsettingdata.md) ", die die zu verschieben VHDs darstellen. Mit der **Connection** -Eigenschaft dieser Instanzen wird der Ziel Speicherort der virtuellen Festplatte angegeben.

</dd> <dt>

**Newsystemsettingdata**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einer Live Migration wird dies immer auf **null** festgelegt.

Bei einer Speicher Migration werden die Daten Stämme der virtuellen Maschine nicht verschoben, wenn diese **null** ist. Andernfalls enthält Sie eine eingebettete Instanz der [**MSVM-Klasse " \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) ", bei der die Eigenschaften " **externaldataroot**", " **snapshotdataroot**" und " **tauapfiledataroot** " die neuen Daten Stämme angeben.

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer, der nach Abschluss oder Fehler des Auftrags benachrichtigt wird. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**Otherherstellyaction**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Wiederherstellungs Aktion beschreibt, wenn die **Wiederherstellungs Action** -Eigenschaft der-Instanz 1 (Sonstiges) ist. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzer, der den Auftrag übermittelt hat. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MinValue** (0), **MaxValue** (100), **Units** ("Prozent")
</dt> </dl>

Der Abschluss Prozentsatz des Auftrags. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Wichtigkeit der Ausführung eines Auftrags. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Wiederherstellbarkeits Aktion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Wiederherstellungs Aktion, die für einen erfolglos ausgeführten Auftrag ausgeführt werden soll. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Nicht fortsetzen** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Fortfahren mit dem nächsten Auftrag** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Auftrag erneut ausführen** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Wiederherstellungsauftrag ausführen** (5)
</dt> </dl>

</dd> <dt>

**Runday**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MinValue** (-31), **MaxValue** (31)
</dt> </dl>

Der Tag des Monats, an dem der Auftrag verarbeitet werden soll. Abhängig vom Wert von **rundayosweek** gibt es unterschiedliche Interpretationen für diese Eigenschaft.

Wenn **rundayosweek** den Wert 0 hat und **runday** positiv ist, definiert **runday** den Tag des Monats, an dem der Auftrag verarbeitet wird. Wenn **rundayosweek** beispielsweise 0 und **runday** 12 ist, wird der Auftrag am 12 <sup>.</sup> Tag des Monats verarbeitet.

Wenn **rundayosweek** 0 und **runday** negativ ist, definiert **runday** die Anzahl von Tagen vor dem letzten Tag des Monats, an dem der Auftrag verarbeitet wird.  1 gibt den letzten Tag des Monats an, 2 gibt einen Tag vor dem letzten Tag des Monats an usw. Wenn **rundayosweek** beispielsweise 0 und **runday** 1 ist, wird der Auftrag am letzten Tag des Monats verarbeitet.

Wenn **rundayofweek** nicht 0 ist, ist **rundayofweek** der Wochentag, an dem der Auftrag im Verhältnis zum **runday** verarbeitet wird. Wenn **runday** beispielsweise 15 und **rundayosweek** 7 (+ Samstag) ist, wird der Auftrag am ersten Samstag am oder nach <sup>dem 15.</sup> Tag des Monats verarbeitet. Wenn **runday** den Wert 20 hat und **rundayosweek** 7 (Samstag) ist, wird der Auftrag am ersten Samstag am oder vor <sup>dem 20.</sup> Tag des Monats verarbeitet. Wenn **runday** 1 und **rundayosweek** 1 (Sonntag) ist, wird der Auftrag am letzten Sonntag des Monats verarbeitet.

Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Rundayof-Woche**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine positive oder negative ganze Zahl, die zusammen mit **runday** zum Angeben des Wochentags oder Monats, an dem der Auftrag verarbeitet wird, verwendet wird. Weitere Informationen finden Sie in der Beschreibung der **runday** -Eigenschaft. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samstag** (7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Freitag** (6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Donnerstag** (5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mittwoch** (4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Dienstag** (3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Montag** (2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sonntag** (1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Exactdayosmonth** (0)
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

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samstag** (7)
</dt> </dl>

</dd> <dt>

**Runmonth**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Monat, in dem der Auftrag verarbeitet werden soll. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

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

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezember** (11)
</dt> </dl>

</dd> <dt>

**Runstartinterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall nach Mitternacht, zu dem der Auftrag verarbeitet werden soll. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Scheduledstarttime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die geplante Startzeit für den Auftrag, falls zutreffend. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag gestartet wurde. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.

</dd> <dt>

**Timebeforeremoval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeitspanne (in Minuten), die der Auftrag nach Abschluss der Ausführung aufbewahrt wird, entweder erfolgreich oder Fehler in dieser Ausführung. Der Auftrag muss für einige Zeit vorhanden sein, unabhängig vom Wert der **deleteoncompletion** -Eigenschaft. Der Standardwert beträgt fünf Minuten. Diese Eigenschaft wird von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))geerbt und ist immer auf 00000000000500.000000:000 festgelegt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des Auftrags Zustands. Wenn der Status des Auftrags nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden. Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden. Diese Eigenschaft wird von [**CIM " \_ concretejob**](/previous-versions//cc136808(v=vs.85))" geerbt.

</dd> <dt>

**Timesub;**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag übermittelt wurde. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll. Diese Eigenschaft wird vom [**CIM- \_ Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**Virtualsystemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name des betroffenen virtuellen Systems.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

