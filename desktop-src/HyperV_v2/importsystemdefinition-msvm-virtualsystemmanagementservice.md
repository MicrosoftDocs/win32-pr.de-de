---
description: Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Importsystemdefinition-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354596"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Importsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SystemDefinitionFile* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zur System Definitionsdatei (. XML oder. exp), die den zu importierenden virtuellen Computer darstellt. Die Definitionsdatei darf nicht bereits vom Host System oder der Virtualisierungsplattform verwendet werden.

</dd> <dt>

*Snapshotfolder* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zum Ordner, in dem die Momentaufnahme Konfigurationen für diesen virtuellen Computer gefunden werden können. Dieser Ordner wird durchsucht, um Momentaufnahmen zu finden, auf die in der Definition der virtuellen Maschine verwiesen wird. Alle referenzierten Momentaufnahmen, die an diesem Speicherort nicht gefunden werden, müssen mithilfe der [**destroysnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) -Methode gelöscht oder mithilfe der [**importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) -Methode importiert werden, bevor das geplante Computersystem erkannt wird.

</dd> <dt>

*Generatenewsystematidentifier* \[ in\]
</dt> <dd>

Gibt an, ob der eindeutige Bezeichner für den virtuellen Computer wieder verwendet werden soll. Wenn dieser Parameter **true** ist, wird ein neuer System Bezeichner generiert. Wenn dieser Parameter **false** ist, wird der vorhandene System Bezeichner verwendet.

</dd> <dt>

*Importedsystem* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang synchron abgeschlossen wird, ein Verweis auf ein [**MSVM \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Objekt, das den importierten virtuellen Computer darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

**Verwendete Datei** (32779)
</dt> </dl>

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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

