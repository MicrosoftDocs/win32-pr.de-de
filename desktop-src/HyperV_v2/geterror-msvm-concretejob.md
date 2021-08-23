---
description: 'GetError-Methode der Msvm_ConcreteJob-Klasse: Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden.'
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: GetError-Methode der Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c169636931ff0d284d20cb616450a5a716848dd074347f3e96abafd4a153693a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682430"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a>GetError-Methode der Msvm \_ ConcreteJob-Klasse

Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein [**CIM \_ Error-Objekt**](/previous-versions//cc150671(v=vs.85)) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird eine **\_ CIM-Fehlerinstanz** zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Wenn der Betriebsstatus des Auftrags nicht 2 (OK) lautet, gibt diese Methode eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück. Wenn der Betriebsstatus des Auftrags 2 (OK) lautet, wird **NULL** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

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

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ ConcreteJob-Klasse**](msvm-concretejob.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

