---
title: Controls. stoppt-Methode
description: Die Methode "beenden" beendet die Wiedergabe des Medien Elements. | Controls. stoppt-Methode
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- Windows-Media Player "Methode"
- Methode "Methode Media Player", Steuerelement Klasse
- Steuerelement-Klasse, Windows Media Player, Methode "Ende"
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369667"
---
# <a name="controlsstop-method"></a>Controls. stoppt-Methode

Die Methode " **Beenden** " beendet die Wiedergabe des Medien Elements.

## <a name="syntax"></a>Syntax


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode bewirkt, dass Windows Media Player alle verwendeten Systemressourcen, z. b. das Audiogerät, freigibt. Das aktuelle Medien Element wird jedoch nicht freigegeben.

Wenn der Spieler angehalten wird, wird die Nachverfolgung an den Anfang zurückgesetzt. Der Aufruf von **Play** beginnt dann, den Clip von Anfang an wiederzugeben. Verwenden Sie die **Pause** -Methode, um einen Wiedergabe Vorgang anzuhalten, ohne die aktuelle Position zu ändern.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Beenden** zum Beenden der Wiedergabe verwendet. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Steuerelemente. Next**](controls-next.md)
</dt> <dt>

[**Controls. Pause**](controls-pause.md)
</dt> <dt>

[**Controls. Previous**](controls-previous.md)
</dt> </dl>

 

 





