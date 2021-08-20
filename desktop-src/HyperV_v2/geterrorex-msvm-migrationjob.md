---
description: Ruft die Fehlerobjekte für den Migrationsauftrag ab, sofern vorhanden.
ms.assetid: 8526e28c-bfc8-42b3-850c-0a875a52a42c
title: GetErrorEx-Methode der Msvm_MigrationJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a6cb3b1b380708a3be259bfd4f9c6ae07bb7e401506dcfe76f2fcf1299ed5d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995243"
---
# <a name="geterrorex-method-of-the-msvm_migrationjob-class"></a>GetErrorEx-Methode der Msvm \_ MigrationJob-Klasse

Ruft die Fehlerobjekte für den Migrationsauftrag ab, sofern vorhanden. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**\_ Msvm-Fehlerinstanz**](msvm-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird mindestens eine **\_ Msvm-Fehlerinstanz** zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ out\]
</dt> <dd>

Wenn der Betriebsstatus des Auftrags nicht 2 (OK) lautet, gibt diese Methode eine oder mehrere eingebettete Instanzen der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück, die die im Auftrag aufgetretenen Fehler darstellen. Wenn der Betriebsstatus des Auftrags 2 (OK) lautet, wird **NULL** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

 




