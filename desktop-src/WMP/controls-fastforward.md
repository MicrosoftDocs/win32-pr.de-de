---
title: Controls. FastForward-Methode
description: Die FastForward-Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung. | Controls. FastForward-Methode
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- FastForward-Methoden Fenster Media Player
- FastForward-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, FastForward-Methode
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357640"
---
# <a name="controlsfastforward-method"></a>Controls. FastForward-Methode

Die **FastForward** -Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.

## <a name="syntax"></a>Syntax


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **FastForward** -Methode gibt den Clip mit dem fünf fachen der normalen Geschwindigkeit wieder. Durch Aufrufen von **FastForward** werden die *Einstellungen* geändert. **bewerten** Sie die-Eigenschaft auf 5,0. Wenn die **Rate** anschließend geändert wird **oder wenn "** wiedergeben" oder " **Beenden** " aufgerufen wird, wird die schnelle Weiterleitung von Windows Media Player beendet.

Die **FastForward** -Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen. Um zu ermitteln, ob Sie sich in einem Clip schnell vorwärts befinden, nennen Sie **IsAvailable**("FastForward").

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **FastForward** verwendet, um die schnelle Wiedergabe des Medien Elements zu starten. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
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
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Pause**](controls-stop.md)
</dt> <dt>

[**"Settings. Rate"**](settings-rate.md)
</dt> </dl>

 

 





