---
description: Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition des virtuellen Computers.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: ImportSystemDefinition-Methode der Msvm_VirtualSystemManagementService Klasse
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
ms.openlocfilehash: ee8dd5bb7d17684216b747717c0adf32011dafa543f05c91a0c1264da89caf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149736"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>ImportSystemDefinition-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition des virtuellen Computers.

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

*SystemDefinitionFile* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zur Systemdefinitionsdatei (.xml oder EXP), die den zu importierenden virtuellen Computer darstellt. Die Definitionsdatei darf nicht bereits vom Hostsystem oder der Virtualisierungsplattform verwendet werden.

</dd> <dt>

*SnapshotFolder* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zu dem Ordner, in dem sich die Momentaufnahmekonfigurationen für diesen virtuellen Computer befinden. Dieser Ordner wird durchsucht, um alle Momentaufnahmen zu finden, auf die in der Definition des virtuellen Computers verwiesen wird. Alle Momentaufnahmen, auf die an diesem Speicherort nicht verwiesen wird, müssen mit der [**DestroySnapshot-Methode**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) gelöscht oder mit der [**ImportSnapshotDefinitions-Methode**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) importiert werden, bevor das geplante Computersystem realisiert wird.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ In\]
</dt> <dd>

Gibt an, ob der eindeutige Bezeichner für den virtuellen Computer wiederverwendet werden soll. Wenn dieser Parameter **true ist,** wird ein neuer Systembezeichner generiert. Wenn dieser Parameter False **ist,** wird der vorhandene Systembezeichner verwendet.

</dd> <dt>

*ImportedSystem* \[ out\]
</dt> <dd>

Wenn der Vorgang synchron abgeschlossen wird, ein Verweis auf ein [**Msvm \_ PlannedComputerSystem-Objekt,**](msvm-plannedcomputersystem.md) das den importierten virtuellen Computer darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei in Verwendung** (32779)
</dt> </dl>

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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

