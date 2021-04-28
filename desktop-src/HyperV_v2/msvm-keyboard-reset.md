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
ms.openlocfilehash: 14c3166ce57fab4693dec87d3d81a55f1f688aa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111708"
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



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm-Tastatur \_**](msvm-keyboard.md)
</dt> </dl>

 

 




