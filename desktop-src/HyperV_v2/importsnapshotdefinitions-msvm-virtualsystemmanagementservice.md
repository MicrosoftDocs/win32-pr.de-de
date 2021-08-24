---
description: Durchsucht den angegebenen Ordner nach Momentaufnahmedefinitionsdateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: ImportSnapshotDefinitions-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 9cfa20eb845546f58201bdc167cfbe38bd4a3bd0ad327a04e009db4504ce0966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694590"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>ImportSnapshotDefinitions-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Durchsucht den angegebenen Ordner nach Momentaufnahmedefinitionsdateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.

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

*PlannedSystem* \[ In\]
</dt> <dd>

Ein Verweis auf ein [**Msvm \_ PlannedComputerSystem-Objekt, das**](msvm-plannedcomputersystem.md) den geplanten virtuellen Computer darstellt, der auf die zu importierenden Momentaufnahmen verweist.

</dd> <dt>

*SnapshotFolder* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zu dem Ordner, in dem sich die Momentaufnahmekonfigurationen für diesen virtuellen Computer befinden.

</dd> <dt>

*ImportedSnapshots* \[ out\]
</dt> <dd>

Wenn der Vorgang synchron abgeschlossen wird, ein Array von Verweisen auf die [**Msvm \_ VirtualSystemSettingData-Instanzen,**](msvm-virtualsystemsettingdata.md) die die erfolgreich importierten Momentaufnahmen darstellen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**Ungültiger Parameter** (32773)
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

**Verwendete Datei** (32779)
</dt> </dl>

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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

