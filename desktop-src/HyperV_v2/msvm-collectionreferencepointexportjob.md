---
description: Diese Klasse stellt einen Exportvorgangauftrag für einen Auflistungsverweispunkt dar.
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
ms.openlocfilehash: 3baf6405f160401b3a2fe8024861d92560484a513e1c55436f9e149e92daed7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681910"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a>Msvm \_ CollectionReferencePointExportJob-Klasse

Diese Klasse stellt einen Exportvorgangauftrag für einen Auflistungsverweispunkt dar.

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

Die **Msvm \_ CollectionReferencePointExportJob-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ CollectionReferencePointExportJob-Klasse** verfügt über diese Methoden.



| Methode                                                                                  | Beschreibung                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-collectionreferencepointexportjob-geterror.md)                     | Ruft einen Fehler ab.<br/>                     |
| [**GetErrorEx**](msvm-collectionreferencepointexportjob-geterrorex.md)                 | Ruft zusätzliche Fehlerinformationen ab.<br/> |
| [**RequestStateChange**](msvm-collectionreferencepointexportjob-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/>                |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CollectionReferencePointExportJob-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BaseReferencePointGroupId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID des Auflistungsverweispunkts, der als Basis in der Exportoperation verwendet wird.

</dd> <dt>

**Unkündbarem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Auftrag abgebrochen werden kann. Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID der VM-Gruppe, für die Protokolldateien exportiert wurden.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Auftrag**](cim-job.md).**ErrorCode**")
</dt> </dl>

Enthält eine Fehlerzusammenfassungsbeschreibung.

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Exportspeicherort.

</dd> <dt>

**ExportedConfigFilePaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Konfigurationsdatei des virtuellen Computers.

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Instanz-IDs von virtuellen Datenträgern, für die Protokolldateien exportiert wurden.

</dd> <dt>

**ExportedGuestStateFilePaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Gastzustandsdatei des virtuellen Computers.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfade der Protokolldateien, die exportiert wurden.

</dd> <dt>

**ExportedRuntimeFilePaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der exportierten Laufzeitstatusdatei des virtuellen Computers.

</dd> <dt>

**ReferencePointGroupId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID des Auflistungsverweispunkts, der exportiert wird.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

GUID der virtuellen Computer, für die der Exportvorgang ausgeführt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

