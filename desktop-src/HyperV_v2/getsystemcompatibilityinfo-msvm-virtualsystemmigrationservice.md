---
description: Generiert ein undurchsichtiges BLOB von Daten, das Kompatibilitätsinformationen für das angegebene System enthält.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Getsystemcompatibilityinfo-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344258"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Getsystemcompatibilityinfo-Methode der MSVM \_ virtualsystemmigrationservice-Klasse

Generiert ein undurchsichtiges BLOB von Daten, das Kompatibilitätsinformationen für das angegebene System enthält. Diese Methode wird in Verbindung mit der [**checksystemcompatibilityinfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode verwendet, um zu bestimmen, ob eine schnelle oder Live Migration eines virtuellen Computers zu einem anderen Host Computersystem möglich ist, ohne tatsächlich die Migration durchführen zu müssen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, für den Kompatibilitätsinformationen abgerufen werden sollen. Wenn sich dieser Parameter auf das hostingcomputersystem bezieht, können die im *compatibilityinfo* -Parameter zurückgegebenen Daten verwendet werden, um zu bestimmen, ob eine der virtuellen Maschinen auf dem Host Computersystem schnell zu einem anderen Host Computersystem migriert werden kann.

</dd> <dt>

*Compatibilityinfo* \[ vorgenommen\]
</dt> <dd>

Ein undurchsichtiges BLOB von Daten, die an die [**checksystemcompatibilityinfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode auf einem anderen Host Computersystem weitergegeben werden können, um die Kompatibilität zu bestätigen.

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

 

 




