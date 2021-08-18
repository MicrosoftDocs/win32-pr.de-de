---
title: Einstellungen.setMode-Methode
description: Die setMode-Methode legt verschiedene Modi auf aktiv oder inaktiv fest.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setMode-Methode Windows Media Player
- setMode-Methode Windows Media Player , Einstellungen-Klasse
- Einstellungen-Klasse Windows Media Player , setMode-Methode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f504fe429dddf1b3db191545e2f34a3605a8fc390346c8f00afe8c3d005f0277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995320"
---
# <a name="settingssetmode-method"></a>Einstellungen.setMode-Methode

Die **setMode-Methode** legt verschiedene Modi auf aktiv oder inaktiv fest.

## <a name="syntax"></a>Syntax


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*modeName* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des modus angibt, der geändert wird und einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Modus, der angibt, ob die Spuren nach der Wiedergabe bis zum Ende an den Anfang zurückgerundet werden. Der Standardzustand ist TRUE.                                                  |
| loop       | Der Modus, der angibt, ob sich die Sequenz von Spuren selbst wiederholt. Der Standardzustand ist "false".                                                                            |
| showFrame  | Modus, der angibt, ob der nächstgelegene Videoschlüsselrahmen an der aktuellen Position angezeigt wird, wenn er nicht wiedergegeben wird. Der Standardzustand ist "false". Hat keine Auswirkungen auf Audiospuren. |
| Shuffle    | Modus, der angibt, ob die Spuren in zufälliger Reihenfolge wiedergegeben werden. Der Standardzustand ist "false".                                                                            |



 

</dd> <dt>

*state* \[ In\]
</dt> <dd>

**Boolescher Wert,** der angibt, ob der neue angegebene Modus aktiv ist oder nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der ShowFrame-Modus aktiv ist, muss der Player auf den Titelinhalt zugreifen, um den Videoframe abzurufen. Verwenden Sie diesen Modus aus Gründen der Bandbreite vorsichtig, wenn Sie nicht lokale Inhalte wiedergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Für Schleifen- und Shufflemodi Windows Media Player Version 7.0 oder höher. Für autoRewind- und showFrame-Modi Windows Media Player serie 9 oder höher.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> <dt>

[**Einstellungen.getMode**](settings-getmode.md)
</dt> </dl>

 

 





