---
description: Stellt die replikationsspezifischen Einstellungen für einen virtuellen Computer dar.
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
ms.openlocfilehash: 90e16e70f7b5bd0a075ffdef54cf0c591719d4993031f3abee19dd8186ec5996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148253"
---
# <a name="msvm_replicationsettingdata-class"></a>Msvm \_ ReplicationSettingData-Klasse

Stellt die replikationsspezifischen Einstellungen für einen virtuellen Computer dar. Der Client übergibt eine Instanz dieser Klasse an [**Msvm \_ ReplicationService.CreateReplicationRelationship,**](createreplicationrelationship-msvm-replicationservice.md) um eine Replikationsbeziehung zu erstellen. Der Client kann die Werte der Eigenschaften für diese Klasse nicht direkt ändern. Sie muss die [**Msvm \_ ReplicationService.ModifyReplicationSettings-Methode**](modifyreplicationsettings-msvm-replicationservice.md) aufrufen, um die Werte zu ändern. Jede Replikationsbeziehung verfügt über eine einzelne Instanz von Einstellungen.

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

Die **Msvm \_ ReplicationSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ReplicationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalSettings**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Replikationseinstellungen, die der Endpunktanbieter verwenden kann.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**ApplicationConsistentSnapshotInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Zeitintervall zwischen anwendungs konsistenten Momentaufnahmen, angegeben in Stunden. Gültige Werte liegen zwischen 1 Stunde und 12 Stunden.

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Definieren Sie den Authentifizierungsmodus, der zum Herstellen einer Verbindung zum Wiederherstellen des Servers verwendet wird.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos-Authentifizierung** (1)


</dt> <dd>

Kerberos-Authentifizierung.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikatbasierte Authentifizierung** (2)


</dt> <dd>

Zertifikatbasierte Authentifizierung.

</dd> </dl>

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerung bis zum automatischen Start des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Computer angibt, wenn das Hostsystem gestartet wird. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**AutoResynchronizeEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Neusynchronisierungsvorgänge automatisch ausgelöst werden, wenn ein Replikationsfehler aufgrund von Strom- und Hardwarefehlern auftritt. Neusynchronisierungsvorgänge werden nur ausgelöst, wenn der Fehler zwischen den durch die **AutoResynchronizeIntervalStart-** und **AutoResynchronizeIntervalEnd-Eigenschaften** angegebenen Zeiten auftritt.

Der Standardwert ist **False**.

</dd> <dt>

**AutoResynchronizeIntervalEnd**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Endzeit für automatische Neusynchronisierungsvorgänge an, die ausgelöst werden sollen. Dieser Wert ist in Ortszeit. Der Standardwert ist 06:00 (6:00 Uhr).

Neusynchronisierungsvorgänge werden nur ausgelöst, wenn der Fehler zwischen den durch die **AutoResynchronizeIntervalStart-** und **AutoResynchronizeIntervalEnd-Eigenschaften** angegebenen Zeiten auftritt.

Neusynchronisierungsvorgänge können auch so geplant werden, dass sie während des nächsten Intervalls ausgelöst werden.

</dd> <dt>

**AutoResynchronizeIntervalStart**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Startzeit für automatische Neusynchronisierungsvorgänge an, die ausgelöst werden sollen. Dieser Wert ist in Ortszeit. Der Standardwert ist 18:30 (18:30 Uhr).

Neusynchronisierungsvorgänge werden nur ausgelöst, wenn der Fehler zwischen den durch die **AutoResynchronizeIntervalStart-** und **AutoResynchronizeIntervalEnd-Eigenschaften** angegebenen Zeiten auftritt.

Neusynchronisierungsvorgänge können auch so geplant werden, dass sie während des nächsten Intervalls ausgelöst werden.

</dd> <dt>

**BypassProxyServer**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Proxyserver beim Herstellen einer Verbindung mit einem Wiederherstellungsserver umgangen werden soll.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Replication Einstellungen" festgelegt.

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Zertifikatfingerabdruck, der verwendet werden soll, wenn die **AuthenticationType-Eigenschaft** eine zertifikatbasierte Authentifizierung ist.

</dd> <dt>

**CompressionEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Replikationsdaten komprimiert werden, während sie an den Wiederherstellungsserver gesendet werden.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und Dateiname einer Datei, in der Informationen zur Konfiguration des virtuellen Computers gespeichert werden. Dieser Pfad ist relativ zur **ConfigurationDataRoot-Eigenschaft.** Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der die Einstellungen für den virtuellen Computer erstellt wurden. Wenn dieses Objekt die aktuellen Einstellungen für den virtuellen Computer darstellt, wäre dieser Wert der Zeitpunkt, zu dem das System erstellt wurde. Wenn dieses Objekt die Momentaufnahmeeinstellungen für den virtuellen Computer darstellt, wäre dieser Wert der Zeitpunkt, zu dem die Momentaufnahme erstellt wurde. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifySystemSettings-Methode**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Virtual Machine Replication Einstellungen Data" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und auf den Anzeigenamen für den virtuellen Computer festgelegt.

</dd> <dt>

**EnableWriteOrderPreservationAcrossDisks**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert")
</dt> </dl>

Gibt an, ob alle replizierenden virtuellen Festplatten für den virtuellen Computer zum gleichen Zeitpunkt repliziert werden. Dadurch wird sichergestellt, dass bei der Replikation die Schreib reihenfolge der Anwendungen auf dem virtuellen Computer verwendet wird.

**Windows 8.1:** Ab Windows 8.1 und Windows Server 2012 R2 ist diese Eigenschaft veraltet und immer auf **TRUE festgelegt.**

</dd> <dt>

**IncludedDisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Die Liste der virtuellen Festplatten (VHDs), die an das System angefügt sind, das von der Replikations-Engine repliziert wird. Dies ist ein Array von Zeichenfolgen, die jeweils die **InstanceID** der [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) enthalten, die die VHD darstellt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt.**](/previous-versions//cc136911(v=vs.85)) Für Windows 8 ist dies immer auf "Microsoft:*Virtual Machine GUID* \\ HVR" festgelegt. Für Windows 8.1 ist dies auf "Microsoft:*Virtual Machine GUID* \\ HVR<\\ 0/1>" festgelegt. Im Windows 8.1 wert gibt 0 primär und 1 die erweiterte Replikation an. Weitere Informationen zur erweiterten Replikation finden Sie unter [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**Notizen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird nicht verwendet und kann nicht festgelegt werden.

Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**PrimaryConnectionPoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des primären Verbindungspunkts. Bei einem primären Cluster ist dies der Broker-CAP-Name. Bei einem eigenständigen primären Server ist dies der Hostsystemname.

</dd> <dt>

**PrimaryHostSystem**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der vollqualifizierte Domänenname des primären Hostsystems, das den virtuellen Computer hosten soll.

</dd> <dt>

**RecoveryConnectionPoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des Wiederherstellungsverbindungspunkts. Bei einem Wiederherstellungscluster ist dies der Broker-CAP-Name. Bei einem eigenständigen Wiederherstellungsserver ist dies der Hostsystemname.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der wiederherstellungsbezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**RecoveryHistory**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Wiederherstellungsmomentaufnahmen, die auf dem Wiederherstellungsserver gespeichert werden. Gültige Werte liegen zwischen 0 und 24.

</dd> <dt>

**RecoveryHostSystem**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der vollqualifizierte Domänenname des Wiederherstellungshostsystems, das den virtuellen Computer hosten soll.

</dd> <dt>

**RecoveryServerPortNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Portnummer des Wiederherstellungsservers, die beim Herstellen einer sicheren Verbindung für die Replikation verwendet werden soll.

</dd> <dt>

**ReplicateHostKvpItems**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nur hostbasierte [**Msvm \_ KvpExchangeDataItem-Dateien**](msvm-kvpexchangedataitem.md)vom primären virtuellen Computer auf den virtuellen Wiederherstellungscomputer repliziert werden sollen.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Replikationsintervall einer Replikationsbeziehung in Sekunden. Gültige Werte sind:

30

300

900

Der Standardwert ist 300 Sekunden.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**ReplicationProvider**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad zur Instanz der [**Msvm \_ ReplicationProvider-Klasse,**](msvm-replicationprovider.md) die den Replikationsanbieterendpunkt identifiziert.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**RootCertificateThumbPrint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Stammzertifikatfingerabdruck des Zertifikats, das verwendet wird, **wenn AuthenticationType** 2 (zertifikatbasierte Autorisierung) ist.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den informationen zum Angehalten des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Auslagerungsdateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt,**](/previous-versions//cc136954(v=vs.85))aber nicht verwendet.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des [**\_ CIM-ComputerSystemobjekts,**](/windows/desktop/CIMWin32Prov/cim-computersystem) zu dem diese Einstellungsdaten gehören. Diese Eigenschaft ist eine Außerkraftsetzung [**von CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des virtuellen Computers an, den die Einstellungsdaten darstellt. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und immer auf "Microsoft:Hyper-V:Replica" festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

