---
description: Ruft das Fehler Objekt für den Migrations Auftrag ab, sofern vorhanden.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: GetError-Methode der Msvm_MigrationJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349024"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a>GetError-Methode der MSVM \_ migrationjob-Klasse

Ruft das Fehler Objekt für den Migrations Auftrag ab, sofern vorhanden. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85)) Objekt zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, wird eine **CIM- \_ Fehler** Instanz zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ vorgenommen\]
</dt> <dd>

Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode eine eingebettete Instanz der [**MSVM- \_ Fehler**](msvm-error.md) Klasse im CIM-XML-Format zurück. Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **null** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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

Das **System wird verwendet** (32774).
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

[**MSVM \_ migrationjob**](msvm-migrationjob.md)
</dt> </dl>

 

