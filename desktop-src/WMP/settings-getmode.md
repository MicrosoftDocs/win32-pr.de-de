---
title: Einstellungen.getMode-Methode
description: Die getMode-Methode bestimmt, ob der Schleifenmodus oder shuffle-Modus aktiv ist.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- getMode-Methode Windows Media Player
- getMode-Methode Windows Media Player , Einstellungen-Klasse
- Einstellungen-Klasse Windows Media Player , getMode-Methode
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
ms.openlocfilehash: 779c775319cbe0d6dc443b4eb99febd494db3d30fb35228b7310f8f1ae7d691d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995330"
---
# <a name="settingsgetmode-method"></a>Einstellungen.getMode-Methode

Die **getMode-Methode** bestimmt, ob der Schleifenmodus oder shuffle-Modus aktiv ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*modeName* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des betreffenden Modus angibt und einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Spuren werden am Anfang neu gestartet, nachdem sie bis zum Ende wiedergegeben wurden.                                                          |
| loop       | Die Sequenz von Spuren wiederholt sich selbst.                                                                                   |
| showFrame  | Der nächstgelegene Keyframe wird an der aktuellen Position angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob der angegebene Modus aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Für Schleifen- und Shufflemodi Windows Media Player Version 7.0 oder höher. Für autoRewind- und showFrame-Modi Windows Media Player serie 9 oder höher.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> <dt>

[**Einstellungen.setMode**](settings-setmode.md)
</dt> </dl>

 

 





