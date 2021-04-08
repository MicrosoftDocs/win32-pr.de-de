---
description: Überprüft die Kompatibilitätsinformationen auf die Kompatibilität mit dem hostingcomputersystem.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Checksystemcompatibilityinfo-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862080"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Checksystemcompatibilityinfo-Methode der MSVM \_ virtualsystemmigrationservice-Klasse

Überprüft die Kompatibilitätsinformationen auf die Kompatibilität mit dem hostingcomputersystem.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Compatibilityinfo* \[ in\]
</dt> <dd>

Ein BLOB von Daten, die durch Aufrufen der [**getsystemcompatibilityinfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode auf dem hostingcomputersystem abgerufen werden.

</dd> <dt>

*Gründe* \[ vorgenommen\]
</dt> <dd>

Ein Array von Zeichen folgen, das die eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfängt, die Warnungen oder Fehler darstellen.

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

**Nicht kompatibel** (32784)
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

[**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




