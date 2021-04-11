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
# <a name="msvm_replicationsettingdata-class"></a>MSVM \_ replicationsettingdata-Klasse

Stellt die Replikations spezifischen Einstellungen für einen virtuellen Computer dar. Der Client übergibt eine Instanz dieser Klasse an [**MSVM \_ replicationservice. kreatereplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md) , um eine Replikations Beziehung zu erstellen. Der Client kann die Werte einer der Eigenschaften für diese Klasse nicht direkt ändern. Es muss die [**MSVM-Methode \_ replicationservice. modifyreplicationsettings**](modifyreplicationsettings-msvm-replicationservice.md) aufgerufen werden, um die Werte zu ändern. Jede Replikations Beziehung verfügt über eine einzelne Instanz von Einstellungen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **MSVM \_ replicationsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ replicationsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalsettings**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Replikationseinstellungen, die der Endpunkt Anbieter verwenden kann.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Applicationkonsistentsnapshotinterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall zwischen Anwendungs konsistenten Momentaufnahmen (angegeben in Stunden). Gültige Werte liegen zwischen 1 Stunde und 12 Stunden.

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hiermit wird der Authentifizierungsmodus für die Verbindung mit dem Wiederherstellungs Server definiert.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos-Authentifizierung** (1)


</dt> <dd>

Kerberos-Authentifizierung.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung** (2)


</dt> <dd>

Zertifikat basierte Authentifizierung.

</dd> </dl>

</dd> <dt>

**Automatikrecoveryaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Automaticshutdownaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Automaticstartupaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Automaticstartupactiondelay**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Automaticstartupactionsequencenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Autoresynchronizeaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Vorgänge zur erneuten Synchronisierung automatisch ausgelöst werden, wenn ein Replikations Fehler aufgrund von Strom-und Hardwarefehlern auftritt. Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.

Der Standardwert ist **False**.

</dd> <dt>

**Autoresynchronizzutervalend**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Endzeit für die automatische Neusynchronisierung an, die ausgelöst werden soll. Dieser Wert ist Ortszeit. Der Standardwert ist 06:00 (6:00 Uhr).

Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.

Vorgänge zur erneuten Synchronisierung können auch geplant werden, damit Sie während des nächsten Intervalls ausgelöst werden.

</dd> <dt>

**Autoresynchronizeingetervalstart**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Startzeit für die automatische Neusynchronisierung an, die ausgelöst werden soll. Dieser Wert ist Ortszeit. Der Standardwert ist 18:30 (6:30 Uhr).

Vorgänge zur erneuten Synchronisierung werden nur ausgelöst, wenn der Fehler zwischen den von den Eigenschaften **autoresynchronizeintervalstart** und **autoresynchronizeintervalend** angegebenen Zeiten auftritt.

Vorgänge zur erneuten Synchronisierung können auch geplant werden, damit Sie während des nächsten Intervalls ausgelöst werden.

</dd> <dt>

**Bypassproxyserver**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Proxy Server beim Herstellen einer Verbindung mit einem Wiederherstellungs Server umgangen werden soll.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikationseinstellungen" festgelegt.

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Der Zertifikat Fingerabdruck, der verwendet werden soll, wenn die **AuthenticationType** -Eigenschaft eine Zertifikat basierte Authentifizierung ist.

</dd> <dt>

**Compressionaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Replikations Daten beim Senden an den Wiederherstellungs Server komprimiert werden.

</dd> <dt>

**Configurationdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden. Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration der virtuellen Maschine. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Einstellungen für die virtuelle Maschine. Wenn dieses-Objekt die aktuellen Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der das System erstellt wurde. Wenn dieses-Objekt die Momentaufnahme Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der die Momentaufnahme erstellt wurde. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemsettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikations Einstellungsdaten für virtuelle Computer" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und auf den anzeigen Amen für den virtuellen Computer festgelegt.

</dd> <dt>

**Enableschreiteorderkonservierungs ationacrossdisks**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")
</dt> </dl>

Gibt an, ob alle replizierenden virtuellen Festplatten für die virtuelle Maschine auf denselben Zeitpunkt repliziert werden. Dadurch wird sichergestellt, dass die Replikation die Schreib Reihenfolge der Anwendungen auf dem virtuellen Computer berücksichtigt.

**Windows 8.1:** Ab Windows 8.1 und Windows Server 2012 R2 ist diese Eigenschaft veraltet und wird immer auf " **true**" festgelegt.

</dd> <dt>

**Includdisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **hypervembeddedinstance** ("CIM \_ storagezucationsettingdata"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Die Liste der virtuellen Festplatten (VHDs), die mit dem System verbunden sind, das von der Replikations-Engine repliziert wird. Dabei handelt es sich um ein Array von Zeichen folgen, die jeweils die **InstanceId** der " [**MSVM \_ storagebereitungssettingdata**](msvm-storageallocationsettingdata.md) " enthalten, die die VHD darstellt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt. Für Windows 8 ist es immer auf "Microsoft:*Virtual Machine GUID* \\ HVR" festgelegt. Für Windows 8.1 ist die Einstellung "Microsoft:*GUID* \\ HVR \\<0/1>" für den virtuellen Computer. Im Windows 8.1 Wert gibt 0 den primär Wert und 1 die erweiterte Replikation an. Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**Logdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet und kann nicht festgelegt werden.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Primaryconnectionpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des primären Verbindungs Punkts. Bei einem primären Cluster ist dies der Name des Broker-Cap. Bei einem eigenständigen primären Server handelt es sich hierbei um den Namen des Host Systems.

</dd> <dt>

**Primaryhostsystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der voll qualifizierte Domänen Name des primären Host Systems, das den virtuellen Computer hostet.

</dd> <dt>

**Wiederherstellungsconnectionpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des Wiederherstellungs Verbindungs Punkts. Bei einem Wiederherstellungs Cluster handelt es sich hierbei um den Broker-Cap-Namen. Bei einem eigenständigen Wiederherstellungs Server handelt es sich hierbei um den Namen des Host Systems.

</dd> <dt>

**Wiederherstellbare Datei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Parameter recoveryhistory einen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Wiederherstellungs Momentaufnahmen, die auf dem Wiederherstellungs Server gespeichert werden. Gültige Werte sind 0 bis 24.

</dd> <dt>

**Wiederherstellunghostsystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der voll qualifizierte Domänen Name des Wiederherstellungs Host Systems, das den virtuellen Computer hostet.

</dd> <dt>

**Wiederherstellserverportnummer**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Portnummer des Wiederherstellungs Servers, die beim Herstellen einer sicheren Verbindung für die Replikation verwendet werden soll.

</dd> <dt>

**Replicatehostkvpitems**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nur Host- [**MSVM \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md)s vom primären virtuellen Computer auf den virtuellen Wiederherstellungs Computer repliziert werden soll.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Replikations Intervall einer Replikations Beziehung in Sekunden. Gültige Werte sind:

30

300

900

Der Standardwert ist 300 Sekunden.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Replicationprovider**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad zur Instanz der [**MSVM- \_ replicationprovider**](msvm-replicationprovider.md) -Klasse, die den Endpunkt des Replikations Anbieters identifiziert.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Rootcertifialisiethumschlag-Print**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Der Fingerabdruck des Stamm Zertifikats des verwendeten Zertifikats, wenn " **AuthenticationType** " den Wert "2" hat (Zertifikat basierte Autorisierung).

</dd> <dt>

**Snapshotdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Suspenddataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Austauschen von Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören. Diese Eigenschaft ist eine außer Kraft Setzung von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Virtualsystemtype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und ist immer auf "Microsoft: Hyper-V: Replica" festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**Modifyreplicationsettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

