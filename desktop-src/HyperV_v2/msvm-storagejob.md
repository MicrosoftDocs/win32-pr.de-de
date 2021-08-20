---
description: Stellt einen Speichervorgangsauftrag dar, der vom Microsoft Hyper-V Image Management Service erstellt wurde.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Msvm_StorageJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 740f5ab4df3e26c408aa94c607073f497c1458fa66a67958736945887dffd1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950129"
---
# <a name="msvm_storagejob-class"></a>Msvm \_ StorageJob-Klasse

Stellt einen Speichervorgangsauftrag dar, der vom Microsoft Hyper-V Image Management Service erstellt wurde.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ StorageJob-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ StorageJob-Klasse** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetError**](msvm-storagejob-geterror.md)                     | Ruft den Fehler ab, der den Grund für den Auftragsfehler beschreibt.<br/>                                                                                                                                                                                                                                               |
| [**GetErrorEx**](geterrorex-msvm-storagejob.md)                 | Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**\_ Msvm-Fehlerinstanz**](msvm-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird mindestens eine **\_ Msvm-Fehlerinstanz** zurückgegeben.<br/> |
| **KillJob**                                                      | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                   |
| [**RequestStateChange**](msvm-storagejob-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ StorageJob-Klasse** verfügt über diese Eigenschaften.

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

**Untergeordnet**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einem Fehler des asynchronen Vorgangs enthält diese Eigenschaft den vollständigen Pfad des untergeordneten Objekts der VHD, die von diesem Vorgang betroffen ist.

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

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** durch zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeitdauer, die der Auftrag ausgeführt wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

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

Eine zusammenfassende Beschreibung des Fehlers( falls vorhanden). Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

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
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**JobCompletionStatusCode**
</dt> <dd> <dl> <dt>

Datentyp: **UINT32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der **HRESULT-Code,** der den Abschlussstatus für den asynchronen Vorgang beschreibt.

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie oft der Auftrag ausgeführt werden soll. Der Wert 1 gibt an, dass der Auftrag nicht wiederholt wird, während jeder Wert ungleich 0 (null) einen Grenzwert für die Anzahl der Wiederholungen des Auftrags angibt. 0 (null) gibt an, dass es keine Beschränkung gibt, wie oft der Auftrag verarbeitet werden kann. Er wird jedoch entweder beendet, nachdem **UntilTime** erreicht wurde oder der Auftrag manuell beendet wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Betriebszustand eines Auftrags. Sie kann auch Übergänge zwischen diesen Zuständen angeben, z. B. 6 (Herunterfahren) und 3 (Wird gestartet). Diese Eigenschaft wird von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))geerbt.



| Wert                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Neu**</dt> <dt>2</dt> </dl>                                                               | Der Auftrag wurde noch nie gestartet.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Ab**</dt> <dt>3</dt> </dl>                                           | Der Auftrag wechselt vom Status "Neu", "Angehalten" oder "Dienst" in den Status "Wird ausgeführt".<br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Ausführen von**</dt> <dt>4</dt> </dl>                                               | Der Auftrag wird ausgeführt.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Angehalten 5**</dt> <dt></dt> </dl>                                       | Der Auftrag wird beendet, kann aber nahtlos neu gestartet werden.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Herunterfahren**</dt> <dt>6</dt> </dl>                       | Der Auftrag wechselt in den Zustand "Abgeschlossen", "Beendet" oder "Beendet".<br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Abgeschlossen**</dt> <dt>7</dt> </dl>                                       | Der Auftrag wurde normal abgeschlossen.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Beendet 8**</dt> <dt></dt> </dl>                                   | Der Auftrag wurde durch eine Änderungsanforderung des Status "Terminate" beendet. Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden. Die Anforderung, dass der Auftrag nur als neuer Auftrag neu gestartet werden muss, ist auftragsspezifisch.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**9 wurde gelöscht**</dt> <dt></dt> </dl>                                                   | Der Auftrag wurde durch eine Statusänderungsanforderung "Kill" beendet. Zugrunde liegende Prozesse werden möglicherweise noch ausgeführt, und möglicherweise ist eine Bereinigung erforderlich, um Ressourcen frei zu machen.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Ausnahme**</dt> <dt>10</dt> </dl>                                      | Der Auftrag befindet sich in einem ungewöhnlichen Zustand, der auf einen Fehlerzustand hindeuten kann. Der tatsächliche Status des Auftrags kann über auftragsspezifische Objekte verfügbar sein.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Dienst**</dt> <dt>11</dt> </dl>                                              | Der Auftrag befindet sich in einem anbieterspezifischen Zustand, der die Problemermittlung, -lösung oder beides unterstützt.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>12 32767</dt> </dl>                | Reserviert.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Reservierter Anbieter**</dt> <dt>32768 65535</dt> </dl> | Reserviert.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**Auftragsstatus**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Auftragsstatus darstellt. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des asynchronen Vorgangs, der von dieser Instanz von **Msvm \_ StorageJob** nachverfolgt wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD-Erstellung** (1)


</dt> <dd>

Erstellen eines VHD-Images (Virtuelle Festplatte).

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>Floppy Creation (2) **(Diskettenerstellung** (2))


</dt> <dd>

Erstellen eines virtuellen Diskettenimages (VFD).

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Komprimierung** (3)


</dt> <dd>

Komprimieren der Größe eines VHD-Images.

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Erweiterung** (4)


</dt> <dd>

Erweitern der Größe eines VHD-Images.

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Zusammenführen** (5)


</dt> <dd>

Zusammenführen mehrerer VHD-Images zu einem einzelnen Image.

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Konvertierung** (6)


</dt> <dd>

Konvertieren des Typs eines virtuellen Festplattenimages.

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback-Bereitstellung** (7)


</dt> <dd>

Einbinden der virtuellen Festplatte auf der übergeordneten Partition

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Abrufen von VHD-Informationen** (8)


</dt> <dd>

Einbinden der VHD im Verwaltungsbetriebssystem.

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>Überprüfen des **VHD-Images** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die in den Eigenschaften **RunStartInterval** und **UntilTime** dargestellten Uhrzeiten lokale Zeiten oder UTC-Zeiten darstellen. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ortszeit** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC-Zeit** (2 )
</dt> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bei einem Fehler des asynchronen Vorgangs enthält diese Eigenschaft den Dateipfad zum übergeordneten Element der VHD, die von diesem Vorgang betroffen ist.

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

Beschreibt die Wiederherstellungsaktion, die für einen Auftrag ausgeführt werden soll, der nicht erfolgreich ausgeführt wurde. Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

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

Diese Eigenschaft wird vom [**\_ CIM-Auftrag**](/windows/desktop/CIMWin32Prov/cim-job)geerbt.

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

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Der Zeitpunkt, zu dem der Zustand des virtuellen Computers zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ StorageJob-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

