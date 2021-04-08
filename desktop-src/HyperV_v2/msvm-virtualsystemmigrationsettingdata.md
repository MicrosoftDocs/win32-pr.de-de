---
description: Stellt die Migrations Einstellungen zum Migrieren eines virtuellen Systems und des Speichers dar, der an ein virtuelles System angeschlossen ist.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862055"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>MSVM \_ virtualsystemmigrationsettingdata-Klasse

Stellt die Migrations Einstellungen zum Migrieren eines virtuellen Systems und des Speichers dar, der an ein virtuelles System angeschlossen ist.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Zuweisung von Dateien"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Hiermit wird der Speicher Migrations Vorgang ermöglicht, vorhandene vhdx-Dateien zu überschreiben.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**Vermeidremuvingvhds**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Entfernen Sie während der Migration keine VHDs, d. h. VHDs auf der Quelle in erfolgreich und VHDs auf dem Ziel Fehler.

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Bandwidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Bandbreite an, die einem virtuellen System Migrations Vorgang zugewiesen oder angefordert wurde. Die Bandbreiten Einheiten werden durch die **bandwidthunit** -Eigenschaft angegeben. Innerhalb einer Migration gibt der Wert 0 die Standard Bandbreite an. Andernfalls gibt der Wert 0 an, dass keine Bandbreiten unterstützt werden.

**Bandbreite** und **Priorität** können zusammen verwendet werden. Migrationsprozesse mit dem höchsten Wert für die gleiche Priorität haben die verfügbare Bandbreite basierend auf der angeforderten Bandbreite gemeinsam. Wenn nicht die gesamte Bandbreite von diesem Satz von Prozessen beansprucht wird, wird die verbleibende Bandbreite von Migrationsprozessen mit der nächst niedrigeren gleichen Priorität gemeinsam genutzt. Wenn noch mehr Bandbreite übrig bleibt, werden Migrationsprozesse mit der nächst niedrigeren gleichen Priorität als gleich betrachtet usw.

Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

</dd> <dt>

**Bandwidthunit**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Einheiten an, die von der **Bandbreiten** Eigenschaft verwendet werden. Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert.

Wenn der Wert dieser Eigenschaft "Prozent" ist, muss der Wert der **Bandbreiten** Eigenschaft zwischen 0 und 100 liegen, wobei höhere Werte eine höhere Bandbreite angeben. Der Wert 100 gibt die gesamte verfügbare Bandbreite für die Durchführung von virtuellen System Migrations Vorgängen an. Werte zwischen 1 und 100 sollten linear mit dem verfügbaren Bandbreiten Bereich korrelieren. Beispielsweise sollte der Wert 50 die Hälfte der verfügbaren Bandbreite anfordern.

Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

</dd> <dt>

**Cancelifblackoutcedoldexcegetretenen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bricht die Migration ab, wenn der Schwellenwert für den Blackout überschritten wird.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Cpucappingmagnitude**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("cpucappingmagnitude")
</dt> </dl>

Grad der CPU-capperung während der Migration.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Normal** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Niedrig** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Hoch** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Destinationipaddresslist**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dieser Wert wird für die Speicher Migration **null** sein. Bei der Migration virtueller Systeme kann dies eine Liste der IP-Adressen des Zielhosts enthalten.

</dd> <dt>

**Destinationplannedvirtualsystemid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wenn eine geplante virtuelle Maschine am Migrations Ziel vorhanden ist, wird diese Eigenschaft auf die GUID des geplanten virtuellen Ziel Computers festgelegt, auf dem die virtuelle Maschine migriert werden muss. Dies ist hilfreich in Fällen, in denen ein Benutzer einen geplanten virtuellen Computer am Ziel zusammen mit der Ressourcen Einrichtung erstellt hat und möchte, dass ein virtueller Computer aus der Quelle zu dieser geplanten virtuellen Maschine migriert wird.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Live Migrations Datenverkehr komprimiert werden soll. **True** gibt an, dass komprimiert werden soll andernfalls **false**.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("migrationType")
</dt> </dl>

Gibt den Typ des auszuführenden Migrations Vorgangs an. Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**Virtualsystem** (32768)


</dt> <dd>

Migriert das virtuelle System zum Zielhost.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Speicher** (32769)


</dt> <dd>

Migriert nur die Speicherressourcen des virtuellen Systems.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Gestaffelt** (32770)


</dt> <dd>

Mit der Konfiguration des virtuellen Systems wird ein geplantes virtuelles System auf dem Zielhost erstellt.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**Virtualsystemandstorage** (32771)


</dt> <dd>

Migriert das virtuelle System und seinen Speicher auf den Zielhost.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**Storagedeepcheck** (32772)


</dt> <dd>

Führt eine Überprüfung der Verfügbarkeit virtueller Systemspeicher Ressourcen auf dem Zielhost durch.

</dd> </dl>

</dd> <dt>

**Othertransporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Transporttyp an, der angewendet werden soll, wenn der Wert von **TransportType** 1 (Sonstiges) ist. Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt eine relative Migrations Wichtigkeit an, die das Migrationssystem möglicherweise verwendet, um mehrere ausstehende Migrations Anforderungen zu sortieren oder anderweitig zu bevorzugen. Je niedriger der Wert, desto höher ist die Priorität. Innerhalb einer Migration gibt der Wert 0 die Standardpriorität an. Andernfalls gibt der Wert 0 an, dass Prioritäten nicht unterstützt werden.

Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

</dd> <dt>

**Removesourceunmanagedvhds**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Entfernen von nicht verwalteten Quell-VHDs.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Retainvhdcopiesonsource**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bei einer Speicher Migration geben Sie an, ob die schreibgeschützten VHDs auf dem Quellhost nach Abschluss der Migration entfernt werden sollen.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("TransportType")
</dt> </dl>

Gibt den Transporttyp an, der für einen virtuellen System Migrations Vorgang angewendet werden soll. Diese Eigenschaft wird von **CIM \_ virtualsystemmigrationsettingdata** geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768..)


</dt> <dd></dd> </dl>

Bei der Live Migration gibt diese Eigenschaft den Transporttyp an, der zum Übertragen des Zustands des virtuellen Systems auf den Zielhost verwendet werden soll. Die unterstützten Werte sind:

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Gibt den TCP-Transporttyp an.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Gibt den Transporttyp für die Übertragung des Zustands der virtuellen Maschine an SMB.

</dd> </dl>

</dd> <dt>

**Unmanagedvhds**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ fiveunmanagedvhd")
</dt> </dl>

Ein Array von eingebetteten [**MSVM \_ -MSVM**](msvm-moveunmanagedvhd.md) -Instanzen, die nicht verwaltete VHDs-Informationen enthalten.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

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

[**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

