---
description: Ruft den Schlüssel Zustand eines Schlüssels ab.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Iskeypressed-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215131"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Iskeypressed-Methode der MSVM- \_ Tastatur Klasse

Ruft den Schlüssel Zustand eines Schlüssels ab.

## <a name="syntax"></a>Syntax


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keycode* \[ in\]
</dt> <dd>

Typ: **UInt32**

Der virtuelle Schlüsselcode des abzufragende Schlüssels. Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.

</dd> <dt>

*KeyState* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Der aktuelle Zustand des Schlüssels. Ein **true** -Wert bedeutet, dass der Schlüssel nicht angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich NULL gibt an, dass der Schlüssel Zustand nicht abgefragt werden konnte.

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

## <a name="remarks"></a>Bemerkungen

Die **iskeypressed** -Methode gibt immer **false** für das **VK- \_ Menü** (18), **VK- \_ Steuer** Element (17) und **VK \_ Shift** (16) zurück, da es sich hierbei nicht um echte Tasten auf einer Tastatur handelt. Diese virtuellen Schlüsselcodes werden immer " **VK \_ lmenu** (164)", **" \_ VK lcontrol** (162)" und " **VK \_ LShift** (160)" durch die Methoden " [**presskey**](presskey-msvm-keyboard.md) " und " [**releasekey**](releasekey-msvm-keyboard.md) " zugeordnet.

Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM- \_ Tastatur**](msvm-keyboard.md)
</dt> <dt>

[**Codes von virtuellen Schlüsseln**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

