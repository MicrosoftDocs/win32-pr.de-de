---
title: Settings. setmode-Methode
description: Die setmode-Methode legt verschiedene Modi auf aktiv oder inaktiv fest.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setmode-Methode, Windows-Media Player
- setmode-Methode, Windows Media Player, Einstellungs Klasse
- Einstellungs Klasse, Windows Media Player, setmode-Methode
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
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356444"
---
# <a name="settingssetmode-method"></a>Settings. setmode-Methode

Die **setmode** -Methode legt verschiedene Modi auf aktiv oder inaktiv fest.

## <a name="syntax"></a>Syntax


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Namen des geänderten Modus angibt, der einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autorewind | Der Modus, der angibt, ob die Nachverfolgung an den Anfang nach dem Ende wiederholt wird. Der Standardstatus ist "true".                                                  |
| loop       | Der Modus, der angibt, ob sich die Reihenfolge der Spuren wiederholt Der Standardstatus ist false.                                                                            |
| showframe  | Modus, der angibt, ob der nächste Video Keyframe an der aktuellen Position angezeigt wird, wenn er nicht wiedergegeben wird. Der Standardstatus ist false. Hat keine Auswirkung auf Audiospuren. |
| Shuffle    | Modus, der angibt, ob die Spuren in zufälliger Reihenfolge wiedergegeben werden Der Standardstatus ist false.                                                                            |



 

</dd> <dt>

*Status* \[ in\]
</dt> <dd>

**Boolescher** Wert, der angibt, ob der neue angegebene Modus aktiv ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der showframe-Modus aktiv ist, muss der Spieler auf den Inhalt des Titels zugreifen, um den Videoframe abzurufen. Aufgrund von Bandbreiten Überlegungen sollten Sie diesen Modus bei der Wiedergabe nicht lokaler Inhalte vorsichtig verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Für Schleifen-und Shuffle-Modi ist Windows Media Player Version 7,0 oder höher. Für den Modus "autorewind" und "showframe", Windows Media Player 9 oder höher.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> </dl>

 

 





