---
description: Diese Klasse stellt einen Sammlungs Referenz-Export Vorgangs Auftrag dar.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349718"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a>MSVM \_ collectionreferencepointexportjob-Klasse

Diese Klasse stellt einen Sammlungs Referenz-Export Vorgangs Auftrag dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-collectionreferencepointexportjob-geterror.md)                     | Ruft einen Fehler ab.<br/>                     |
| [**Geterrorex**](msvm-collectionreferencepointexportjob-geterrorex.md)                 | Ruft zusätzliche Fehlerinformationen ab.<br/> |
| [**RequestStateChange**](msvm-collectionreferencepointexportjob-requeststatechange.md) | Fordert eine Statusänderung an.<br/>                |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Basereferencepointgroupid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID des Auflistungs Verweis Punkts, der als Basis in "Exportoperation" verwendet wird.

</dd> <dt>

**Abbrechbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag abgebrochen werden kann. Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.

</dd> <dt>

**Sammlungs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID der virtuellen Computergruppe, für die Protokolldateien wereexportiert werden.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")
</dt> </dl>

Enthält eine Beschreibung der Fehler Zusammenfassung.

</dd> <dt>

**Exportdirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Export Speicherort.

</dd> <dt>

**Exportedconfigfilepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Konfigurationsdatei des virtuellen Computers.

</dd> <dt>

**Exporteddisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Instanz-IDs von virtuellen Datenträgern, für die Protokolldateien exportiert wurden.

</dd> <dt>

**Exportedgueststatefilepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Gast Zustands Datei der virtuellen Maschine.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Exportedlogfilepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfade der Protokolldateien, die exportiert wurden.

</dd> <dt>

**Exportedruntimefilepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Lauf Zeit Zustands Datei des virtuellen Computers.

</dd> <dt>

**Referencepointgroupid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID des Sammlungs Verweis Punkts, der exportiert wird.

</dd> <dt>

**Virtualmachineid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID der virtuellen Computer, für die der Export Vorgang durchgeführt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ concretejob**](cim-concretejob.md)
</dt> </dl>

 

