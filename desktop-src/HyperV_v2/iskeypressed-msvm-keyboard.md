---
description: Ruft den Schlüsselzustand eines Schlüssels ab.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: IsKeyPressed-Methode der Msvm_Keyboard-Klasse
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
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392443"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>IsKeyPressed-Methode der \_ Msvm-Tastaturklasse

Ruft den Schlüsselzustand eines Schlüssels ab.

## <a name="syntax"></a>Syntax


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keyCode* \[ In\]
</dt> <dd>

Typ: **uint32**

Der virtuelle Schlüsselcode des abzufragende Schlüssels. Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*keyState* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Der aktuelle Abwärtszustand des Schlüssels. Ein **True-Wert** bedeutet, dass der Schlüssel ausgeschaltet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass der Schlüsselzustand nicht abgefragt werden kann.

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

Die **IsKeyPressed-Methode** gibt immer **False** für das **VK \_ MENU** (18), **VK \_ CONTROL** (17) und **VK \_ SHIFT** (16) zurück, da es sich hierbei nicht um echte Tasten auf einer Tastatur handelt. Diese Codes für virtuelle Schlüssel werden immer **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) bzw. **VK \_ LSHIFT** (160) durch die [**PressKey-**](presskey-msvm-keyboard.md) und [**ReleaseKey-Methoden**](releasekey-msvm-keyboard.md) zugeordnet.

Der Zugriff auf die [**\_ Msvm-Tastaturklasse**](msvm-keyboard.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**\_Msvm-Tastatur**](msvm-keyboard.md)
</dt> <dt>

[**Codes für virtuelle Schlüssel**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

