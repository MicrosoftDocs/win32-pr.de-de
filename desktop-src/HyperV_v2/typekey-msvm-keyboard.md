---
description: Simuliert eine Tastensequenz für die Veröffentlichung.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: TypeKey-Methode der Msvm_Keyboard Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d387e1b0d0d939d997589c90195b4a50427f1973eaf46520a0fa70caf62c610b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068350"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>TypeKey-Methode der Msvm \_ Keyboard-Klasse

Simuliert eine Tastensequenz für die Veröffentlichung. Dies entspricht dem Aufruf von [**PressKey**](presskey-msvm-keyboard.md) gefolgt von [**ReleaseKey.**](releasekey-msvm-keyboard.md)

## <a name="syntax"></a>Syntax


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keyCode* \[ In\]
</dt> <dd>

Typ: **uint32**

Der virtuelle Schlüsselcode der zu drückenden Taste. Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Codes für virtuelle Schlüssel.**](../inputdev/virtual-key-codes.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass der Schlüsselzustand nicht geändert werden kann.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
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

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**\_ Msvm-Tastaturklasse**](msvm-keyboard.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm-Tastatur \_**](msvm-keyboard.md)
</dt> <dt>

[**Codes für virtuelle Schlüssel**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

