---
title: Controls.isAvailable
description: Die isAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann. | Controls.isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controls.isAvailable Windows Media Player
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
ms.openlocfilehash: 502343b7654241a00e9efb33acc6f5de842c6fb6bad650f24839a5fe7febf9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135743"
---
# <a name="controlsisavailable"></a>Controls.isAvailable

Die **isAvailable-Eigenschaft** gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parameter

*name*

**Eine Zeichenfolge,** die einen der folgenden Werte enthält.



| Zeichenfolge          | Beschreibung                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Bestimmt, ob der Benutzer die **currentItem-Eigenschaft festlegen** kann.                                                                                                 |
| currentMarker   | Bestimmt, ob der Benutzer nach einem bestimmten Marker suchen kann.                                                                                                        |
| currentPosition | Bestimmt, ob der Benutzer eine bestimmte Position in der Datei suchen kann. Einige Dateien unterstützen keine Suchunterstützung.                                                       |
| Fastforward     | Bestimmt, ob die Datei die schnelle Weiterleitung unterstützt und ob diese Funktionalität aufgerufen werden kann. Viele Dateitypen (oder Livestreams) unterstützen fastForward nicht. |
| fastReverse     | Bestimmt, ob die Datei fastReverse unterstützt und ob diese Funktionalität aufgerufen werden kann. Viele Dateitypen (oder Livestreams) unterstützen fastReverse nicht.     |
| Weiter            | Bestimmt, ob der Benutzer nach dem nächsten Eintrag in einer Wiedergabeliste suchen kann.                                                                                             |
| pause           | Bestimmt, ob die **pause-Methode** verfügbar ist.                                                                                                             |
| Spielen            | Bestimmt, ob die **Wiedergabemethode** verfügbar ist.                                                                                                              |
| Vorherige        | Bestimmt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.                                                                                         |
| Schritt            | Bestimmt, ob **die Schrittmethode** während der Wiedergabe verfügbar ist.                                                                                              |
| stop            | Bestimmt, ob **die Stop-Methode** verfügbar ist.                                                                                                              |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen **booleschen Wert** zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das nach der Anfangsposition des aktuellen Medienelements sucht. Der JScript code verwendet **isAvailable,** um zu überprüfen, ob die Datei den Suchvorgang unterstützt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





