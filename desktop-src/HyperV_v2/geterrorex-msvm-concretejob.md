---
description: 'GetErrorEx-Methode der Msvm_ConcreteJob Klasse: Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden.'
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: GetErrorEx-Methode der Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 67abbd06fdaae9c23cca53f5516586f45216f20d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119348"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a>GetErrorEx-Methode der Msvm \_ ConcreteJob-Klasse

Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden. Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück. Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird mindestens eine **Msvm \_ Error-Instanz** zurückgegeben.

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

Typ: **\[ \] Zeichenfolge**

Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode mindestens eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück, die die im Auftrag aufgetretenen Fehler darstellen. Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **NULL** zurückgegeben.

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

**Ungültiger** Parameter (32773)
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

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**Msvm \_ ConcreteJob-Klasse**](msvm-concretejob.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 8 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2012-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

