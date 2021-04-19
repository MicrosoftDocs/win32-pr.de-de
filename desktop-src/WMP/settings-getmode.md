---
title: Settings. getMode-Methode
description: Die getMode-Methode bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- getMode-Methode, Windows-Media Player
- getMode-Methode, Windows Media Player, Einstellungs Klasse
- Settings-Klasse, Windows Media Player, getMode-Methode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352957"
---
# <a name="settingsgetmode-method"></a>Settings. getMode-Methode

Die **getMode** -Methode bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Namen des fraglichen Modus angibt, der einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autorewind | Nach der Wiedergabe am Ende werden nachverfolgt.                                                          |
| loop       | Die Reihenfolge der Spuren wird wiederholt.                                                                                   |
| showframe  | Der nächste Keyframe wird an der aktuellen Position angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob der angegebene Modus aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Für Schleifen-und Shuffle-Modi ist Windows Media Player Version 7,0 oder höher. Für den Modus "autorewind" und "showframe", Windows Media Player 9 oder höher.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Settings. setmode**](settings-setmode.md)
</dt> </dl>

 

 





