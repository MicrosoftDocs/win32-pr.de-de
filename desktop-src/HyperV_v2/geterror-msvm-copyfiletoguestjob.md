---
description: 'Msvm_CopyFileToGuestJob::GetError-Methode: Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob::GetError-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119368"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a>Msvm \_ CopyFileToGuestJob::GetError-Methode

Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein [**\_ CIM-Fehlerobjekt**](/previous-versions//cc150671(v=vs.85)) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird eine **\_ CIM-Fehlerinstanz** zurückgegeben.

## <a name="syntax"></a>Syntax


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ out\]
</dt> <dd>

Wenn der Betriebsstatus des Auftrags nicht 2 (OK) lautet, gibt diese Methode eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück. Wenn der Betriebsstatus des Auftrags 2 (OK) lautet, wird **NULL** zurückgegeben.

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



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

