---
description: Ruft eine Liste von MSVM- \_ compatibilityvector-Instanzen ab, die verwendet werden können, um die Kompatibilität des virtuellen Computers (VM) zu überprüfen.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService:: getsystemcompatibilityvectors-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958750"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>MSVM \_ virtualsystemmigrationservice:: getsystemcompatibilityvectors-Methode

Ruft eine Liste von [**MSVM- \_ compatibilityvector**](msvm-compatibilityvector.md) -Instanzen ab, die verwendet werden können, um die Kompatibilität des virtuellen Computers (VM) zu überprüfen.

## <a name="syntax"></a>Syntax


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Abrufen von Kompatibilitäts Vektoren darstellt. Wenn sich dieser Parameter auf das hostingcomputersystem bezieht, können die im *compatibilityvectors* -Parameter zurückgegebenen Daten verwendet werden, um zu bestimmen, ob eine der VMS auf dem Host Computersystem schnell zu einem anderen Host Computersystem migriert werden kann.

</dd> <dt>

*Compatibilityvectors* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**MSVM \_ compatibilityvector**](msvm-compatibilityvector.md) -Instanzen, die die Kompatibilitätsinformationen für die VMs oder das hostingcomputersystem enthalten.

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
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Getsystemcompatibilityvectors** ruft Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei Ausführen auf einem Host Computersystem) ab. Die Kompatibilitätsinformationen bleiben für den Client nicht transparent, während die Informationen eine Möglichkeit bieten, die Host Kompatibilitätsinformationen mit der des virtuellen Computers zu vergleichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Stammvirtualisierung \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ compatibilityvector**](msvm-compatibilityvector.md)
</dt> <dt>

[**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




