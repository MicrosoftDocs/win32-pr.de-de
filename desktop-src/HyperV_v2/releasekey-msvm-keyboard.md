---
description: Simuliert eine Schlüssel Version.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Releasekey-Methode der Msvm_Keyboard-Klasse
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
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530101"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Releasekey-Methode der MSVM- \_ Tastatur Klasse

Simuliert eine Schlüssel Version. Bei erfolgreicher Ausführung befindet sich der Schlüssel im Status "up".

## <a name="syntax"></a>Syntax


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keycode* \[ in\]
</dt> <dd>

Typ: **UInt32**

Der virtuelle Schlüsselcode des zu veröffentlichenden Schlüssels. Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass der Schlüssel Zustand nicht geändert werden konnte.

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

Die **releasekey** -Methode ordnet Verweise auf **das VK- \_ Menü** (18), das **VK- \_ Steuer** Element (17) und die **VK- \_ UMSCHALT** Taste (16) auf " **VK \_ lmenu** (164)", " **VK \_ lcontrol** (162)" und " **VK \_ LShift** (160)" **zu \_** **\_** **\_**

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

 

