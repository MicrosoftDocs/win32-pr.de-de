---
description: Generiert ein nicht transparentes Datenblob, das Kompatibilitätsinformationen für das angegebene System enthält.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: GetSystemCompatibilityInfo-Methode der Msvm_VirtualSystemMigrationService-Klasse
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
ms.openlocfilehash: 4866b54bb6f5d5b90d4221b81e8a847e910e4486edc55eb4f932684397072504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392814"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>GetSystemCompatibilityInfo-Methode der Msvm \_ VirtualSystemMigrationService-Klasse

Generiert ein nicht transparentes Datenblob, das Kompatibilitätsinformationen für das angegebene System enthält. Diese Methode wird in Verbindung mit der [**CheckSystemCompatibilityInfo-Methode**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) verwendet, um zu bestimmen, ob eine schnelle oder Livemigration eines virtuellen Computers zu einem anderen Hostcomputersystem möglich ist, ohne die Migration tatsächlich zu versuchen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**Msvm \_ ComputerSystem-Klasse, die**](msvm-computersystem.md) den virtuellen Computer darstellt, für den Kompatibilitätsinformationen abgerufen werden sollen. Wenn dieser Parameter auf das Hostcomputersystem verweist, können die im *CompatibilityInfo-Parameter* zurückgegebenen Daten verwendet werden, um zu bestimmen, ob virtuelle Computer auf dem Hostcomputersystem schnell zu einem anderen Hostcomputersystem migriert werden können.

</dd> <dt>

*CompatibilityInfo* \[ out\]
</dt> <dd>

Ein nicht transparentes Datenblob, das zur Bestätigung der Kompatibilität an die [**CheckSystemCompatibilityInfo-Methode**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) auf einem anderen Hostcomputersystem übergeben werden kann.

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

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




