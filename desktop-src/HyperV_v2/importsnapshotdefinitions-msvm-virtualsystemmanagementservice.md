---
description: Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Importsnapshotdefinitions-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863571"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Importsnapshotdefinitions-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plannedsystem* \[ in\]
</dt> <dd>

Ein Verweis auf ein [**MSVM- \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Objekt, das die geplante virtuelle Maschine darstellt, die auf die zu importierenden Momentaufnahmen verweist.

</dd> <dt>

*Snapshotfolder* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zum Ordner, in dem die Momentaufnahme Konfigurationen für diesen virtuellen Computer gefunden werden können.

</dd> <dt>

*Importedmomentaufnahmen* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang synchron abgeschlossen wird, ein Array von Verweisen auf die [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanzen, die die Momentaufnahmen darstellen, die erfolgreich importiert wurden.

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

 

