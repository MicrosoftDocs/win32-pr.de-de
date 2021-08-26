---
description: Simuliert eine Schlüsselfreigabe.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: ReleaseKey-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1038838ad7ab0c483dd23e77a716da3ffd2474f7a9e8b4fb311b4a141c1ababb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980130"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>ReleaseKey-Methode der \_ Msvm-Tastaturklasse

Simuliert eine Schlüsselfreigabe. Wenn der Schlüssel erfolgreich ist, befindet er sich im Zustand "Up".

## <a name="syntax"></a>Syntax


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keyCode* \[ In\]
</dt> <dd>

Typ: **uint32**

Der virtuelle Schlüsselcode des schlüssels, der veröffentlicht werden soll. Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass der Schlüsselzustand nicht geändert werden kann.

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

Die **ReleaseKey-Methode** ordnet Verweise auf **VK \_ MENU** (18), **VK \_ CONTROL** (17) und **VK \_ SHIFT** (16) **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) bzw. **VK \_ LSHIFT** (160) zu, da die virtuellen Tastencodes **VK \_ MENU,** **VK \_ CONTROL** und **VK \_ SHIFT** auf einer Tastatur nicht reelle Tasten darstellen.

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

 

