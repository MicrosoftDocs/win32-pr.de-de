---
description: Bietet zusätzliche Informationen, die mit der exportsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse verwendet werden können.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344407"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>MSVM \_ virtualsystemexportsettingdata-Klasse

Bietet zusätzliche Informationen, die mit der [**exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet werden können.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemexportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemexportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Backupintent**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Absicht an, wie die exportierten Sicherungs Sätze verwendet werden.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Backupintentpreservechain** (0)


</dt> <dd>

Alle exportierten vollständigen und differenziellen Sicherungs Sätze werden unverändert beibehalten.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Backupintentmerge** (1)


</dt> <dd>

Die exportierten vollständigen und differenziellen Sicherungs Sätze werden zusammengeführt, um vollständige Sicherungs Sätze zu synthetisieren.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Capturelivestate**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welcher Zustand erfasst werden soll, wenn das Ziel des Exports eine laufende VM ist.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**Capturecrashkonsistentstate** (0)


</dt> <dd>

Es werden keine gespeicherten Zustands Dateien für die laufende VM exportiert, sodass Sie in einen Absturz konsistenten Status versetzt wird.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**Capturesavedstate** (1)


</dt> <dd>

Gespeicherte Zustands Dateien für die laufende VM werden zusammen mit der VM-Konfiguration exportiert.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**Captureappkonsistentstate** (2)


</dt> <dd>

Der Anwendungs konsistente Zustand des laufenden virtuellen Computers wird exportiert.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> </dl>

</dd> <dt>

**Copysnapshotconfiguration**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Momentaufnahmen mit dem virtuellen Computer exportiert werden sollen.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**Exportallshots** (0)


</dt> <dd>

Alle Momentaufnahmen werden mit dem virtuellen Computer exportiert.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**Exportnomomentaufnahmen** (1)


</dt> <dd>

Es werden keine Momentaufnahmen mit dem virtuellen Computer exportiert.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**Exportonesnapshot** (2)


</dt> <dd>

Die von der Eigenschaft **snapshotvirtualsystem** identifizierten Momentaufnahmen werden mit der virtuellen Maschine exportiert. Die Eigenschaften **copyvmstorage** und **copyvmruntimeinformation** werden ignoriert, Speicher-und Laufzeitinformationen werden mit dem virtuellen Computer exportiert, und alle differenzierenden VHD-Datenträger werden in eine neue VHD zusammengeführt.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**Exportonesnapshotforbackup** (3)


</dt> <dd>

Die von der **snapshotvirtualsystem** -Eigenschaft identifizierte Momentaufnahme wird zum Zweck der Sicherung des virtuellen Computers exportiert. Die exportierte Konfiguration verwendet die ID der VM.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> </dl>

</dd> <dt>

**Copyvmruntimeinformation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Laufzeitinformationen des virtuellen Computers beim Exportieren der virtuellen Maschine kopiert werden.



| Wert                                                                                | Bedeutung                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Die Laufzeitinformationen der virtuellen Maschine werden kopiert.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Die Laufzeitinformationen für den virtuellen Computer werden nicht kopiert.<br/> |



 

</dd> <dt>

**Copyvmstorage**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Speicher der virtuellen Maschine beim Exportieren der virtuellen Maschine kopiert wird.



| Wert                                                                                | Bedeutung                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Der Speicher der virtuellen Maschine wird kopiert.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Der Speicher des virtuellen Computers wird nicht kopiert.<br/> |



 

</dd> <dt>

**"Kreatevmexportsubdirectory"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob beim Exportieren der virtuellen Maschine ein Unterverzeichnis mit dem Namen der virtuellen Maschine erstellt wird.



| Wert                                                                                | Bedeutung                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Es wird ein Unterverzeichnis erstellt.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Ein Unterverzeichnis wird nicht erstellt.<br/> |



 

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Differenalbackupbase**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Basis für differenziellen Export. Dabei handelt es sich entweder um einen Pfad zu einer [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Instanz, die den Verweis Punkt oder den Pfad zu einer [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanz darstellt, die die Momentaufnahme darstellt, die als Basis für den differenziellen Export verwendet werden soll. Wenn die Eigenschaft **copysnapshotconfiguration** nicht auf 3 (**exportonesnapshotforbackup**) festgelegt ist, wird diese Eigenschaft ignoriert.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Disabledifferenalofignoredstorage**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob differenzierende Datenträger erstellt werden oder nicht, wenn der Speicher beim Export ignoriert wird. Standardmäßig ist diese Einstellung auf "false" festgelegt. Dies bedeutet, dass differenzierende Datenträger für den Speicher erstellt werden, der nicht in das Exportziel kopiert wird.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeige Name für diese Instanz. Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**Excludvirtualharddisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array von MSVM-Instanzen-IDs der [**\_ storagezuordungssettingdata**](msvm-storageallocationsettingdata.md) (rasd), die die virtuellen Festplatten darstellen, die aus dem Export Vorgang ausgeschlossen werden sollen. Wenn mindestens eine der angegebenen IDs keine gültige angefügte virtuelle Festplatte ist, tritt bei dem Vorgang ein Fehler auf.

Die virtuellen Festplatten, auf die diese Eigenschaft verweist, können vom virtuellen Computer und/oder von seinen Momentaufnahmen sein. Der Ausschluss virtueller Festplatten wird nicht unterstützt, wenn die Eigenschaft **copysnapshotconfiguration** auf 0 (exportallsnapshot) festgelegt ist.

Beachten Sie, dass die rasd-Instanz-ID für virtuelle Festplatten den Speicherort darstellt, an den Sie angefügt sind. durch das Ausschließen dieser ID werden alle virtuellen Festplatten ausgeschlossen, die an diesem Speicherort in der Momentaufnahme Struktur der virtuellen Maschine angefügt sind, und zwar unabhängig davon, ob es sich um eine gültige

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Exportforlivemigration**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der exportierte virtuelle Computer bei der Live Migration verwendet werden soll.

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Innerhalb des Gültigkeits Bereichs des instanziierten Namespaces identifiziert verdeckt und eindeutig eine Instanz dieser Klasse. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**Snapshotvirtualsystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Pfad zu einer [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanz, die die Momentaufnahme darstellt, die mit dem virtuellen Computer exportiert werden soll. Wenn die Eigenschaft **copysnapshotconfiguration** nicht auf 2 (exportonesnapshot) festgelegt ist, wird diese Eigenschaft ignoriert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemexportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[Verwaltungs Klassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> <dt>

[**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

