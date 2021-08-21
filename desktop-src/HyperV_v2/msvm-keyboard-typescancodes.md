---
description: Simuliert eine Schlüsselsequenz mithilfe von Scancodes.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: TypeScancodes-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1ca4aebc94ed7571c2b1cda00d5f81ce363396c2960108c441950782558ec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147617"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a>TypeScancodes-Methode der \_ Msvm-Tastaturklasse

Simuliert eine Schlüsselsequenz mithilfe von Scancodes.

## <a name="syntax"></a>Syntax


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Scancodes* \[ In\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Array, das die zu typisierten Scancodes enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt 0 zurück, wenn sie erfolgreich ist. Jeder andere Rückgabewert gibt einen Fehler an. Der Rückgabewert kann einer der folgenden Werte sein.

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

Der Zugriff auf die [**\_ Msvm-Tastaturklasse**](msvm-keyboard.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**\_Msvm-Tastatur**](msvm-keyboard.md)
</dt> </dl>

 

