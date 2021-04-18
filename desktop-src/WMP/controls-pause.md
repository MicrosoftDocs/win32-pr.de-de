---
title: Controls. Pause-Methode
description: Die Pause-Methode hält die Wiedergabe des Medien Elements an. | Controls. Pause-Methode
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- Windows-Media Player für die Methoden Pause
- Pause-Methode, Windows Media Player, Steuerelement Klasse
- Steuerelement-Klasse, Windows-Media Player, anhaltemethode
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371471"
---
# <a name="controlspause-method"></a>Controls. Pause-Methode

Die **Pause** -Methode hält die Wiedergabe des Medien Elements an.

## <a name="syntax"></a>Syntax


```JScript
Controls.pause()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn eine Datei angehalten wird, gibt Windows Media Player keine Systemressourcen, z. b. das Audiogerät, aus.

Bestimmte Medientypen können nicht angehalten werden, z. b. Livestreams. Verwenden Sie-Steuer *Elemente*, um zu bestimmen, ob ein bestimmter Medientyp angehalten werden kann. **IsAvailable (' Pause ')**.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Pause** zum Anhalten der Wiedergabe verwendet. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
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

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> </dl>

 

 





