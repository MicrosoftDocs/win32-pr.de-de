---
title: Controls. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | Controls. IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Steuerelemente. IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370204"
---
# <a name="controlsisavailable"></a>Controls. IsAvailable

Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parameter

*name*

Eine **Zeichenfolge** , die einen der folgenden Werte enthält.



| Zeichenfolge          | Beschreibung                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Bestimmt, **ob der Benutzer die Eigenschaft "** Eigenschaft" festlegen kann.                                                                                                 |
| currentmarker   | Bestimmt, ob der Benutzer einen bestimmten Marker suchen kann.                                                                                                        |
| CurrentPosition | Bestimmt, ob der Benutzer eine bestimmte Position in der Datei suchen kann. Einige Dateien unterstützen keine Suchvorgänge.                                                       |
| FastForward     | Bestimmt, ob die Datei eine schnelle Weiterleitung unterstützt und ob diese Funktion aufgerufen werden kann. FastForward wird von vielen Dateitypen (oder Livestreams) nicht unterstützt. |
| fastreverse     | Bestimmt, ob die Datei fastreverse unterstützt und ob diese Funktion aufgerufen werden kann. Fastreverse wird von vielen Dateitypen (oder Livestreams) nicht unterstützt.     |
| Weiter            | Bestimmt, ob der Benutzer den nächsten Eintrag in einer Wiedergabeliste suchen kann.                                                                                             |
| pause           | Bestimmt, ob die **Pause** -Methode verfügbar ist.                                                                                                             |
| Theater            | Bestimmt, ob die **Play** -Methode verfügbar ist.                                                                                                              |
| Vorherige        | Bestimmt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.                                                                                         |
| Schritt            | Bestimmt, ob die **Step** -Methode während der Wiedergabe verfügbar ist.                                                                                              |
| stop            | Bestimmt, ob die Methode zum **Abbrechen** verfügbar ist.                                                                                                              |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das die Anfangsposition des aktuellen Medien Elements aufsucht. Der JScript-Code verwendet **IsAvailable** , um zu überprüfen, ob die Datei den Suchvorgang unterstützt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





