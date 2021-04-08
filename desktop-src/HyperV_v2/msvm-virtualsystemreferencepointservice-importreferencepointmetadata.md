---
description: Importiert Verweis Punkt Metadaten des virtuellen Systems.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Importreferencepointmetadata-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961202"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Importreferencepointmetadata-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse

Importiert Verweis Punkt Metadaten des virtuellen Systems.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedsystem* \[ in\]
</dt> <dd>

Ein Verweis auf ein [**MSVM- \_ Computersystem**](msvm-computersystem.md) , das das betroffene System beschreibt.

</dd> <dt>

*Configfilepath* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad der Konfigurationsdatei, aus der die Verweis Punkt Metadaten importiert werden.

</dd> <dt>

*Runtimestatefilepath* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad der Lauf Zeit Zustands Datei, von der die Verweis Punkt Metadaten importiert werden.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt entweder 0 (kein Fehler) oder eine der folgenden Fehlermeldungen zurück:

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
</dt> </dl>

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

[**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




