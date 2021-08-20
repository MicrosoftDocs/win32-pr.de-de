---
description: 'Reset-Methode der Msvm_Keyboard Klasse: Setzt die virtuelle Tastatur zurück.'
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Reset-Methode der Msvm_Keyboard Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 65c2e035f40e5e239868c041de92825884e604973437d7331243a81fd4b3a61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811727"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a>Reset-Methode der \_ Msvm-Tastaturklasse

Setzt die virtuelle Tastatur zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert 0 (null) gibt den Erfolg an. Der Rückgabewert 1 gibt einen Fehler an, da die -Methode nicht unterstützt wird.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm-Tastatur \_**](msvm-keyboard.md)
</dt> </dl>

 

 




