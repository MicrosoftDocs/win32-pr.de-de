---
description: Ruft eine Liste der Msvm \_ CompatibilityVector-Instanzen ab, mit denen die Kompatibilität des virtuellen Computers (VM) zum Hosten überprüft werden kann.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService::GetSystemCompatibilityVectors-Methode
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
ms.openlocfilehash: 19eb9fe54c9a20e635d706eff9b22eb0e78cb8347b27fcdcaff0f419e60a6112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427660"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>Msvm \_ VirtualSystemMigrationService::GetSystemCompatibilityVectors-Methode

Ruft eine Liste der [**Msvm \_ CompatibilityVector-Instanzen**](msvm-compatibilityvector.md) ab, die zum Überprüfen der Kompatibilität virtueller Computer (VM) zum Hosten verwendet werden können.

## <a name="syntax"></a>Syntax


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**Msvm \_ ComputerSystem-Klasse, die**](msvm-computersystem.md) den virtuellen Computer darstellt, für den Kompatibilitätsvektoren abgerufen werden sollen. Wenn dieser Parameter auf das Hostcomputersystem verweist, können die im *CompatibilityVectors-Parameter zurückgegebenen* Daten verwendet werden, um zu bestimmen, ob eine der VMs auf dem Hostcomputersystem schnell zu einem anderen Hostcomputersystem migriert werden kann.

</dd> <dt>

*CompatibilityVectors* \[ out\]
</dt> <dd>

Ein Array von [**Msvm \_ CompatibilityVector-Instanzen,**](msvm-compatibilityvector.md) die die Kompatibilitätsinformationen für die VMs oder das Hostcomputersystem enthalten.

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
</dt> </dl>

## <a name="remarks"></a>Hinweise

**GetSystemCompatibilityVectors ruft Kompatibilitätsinformationen** für einen virtuellen Computer (VM) (bei Ausführung auf einem VM-Computersystem) oder einen Host (bei Ausführung auf einem Hostcomputersystem) ab. Die Kompatibilitätsinformationen bleiben für den Client nicht transparent, während die Informationen eine Möglichkeit bieten, die Hostkompatibilitätsinformationen mit denen des virtuellen Computers zu vergleichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




