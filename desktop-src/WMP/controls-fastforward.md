---
title: Controls.fastForward-Methode
description: Die fastForward-Methode startet die schnelle Wiedergabe des Medienelements in vorwärts gerichteter Richtung. | Controls.fastForward-Methode
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- fastForward-Windows Media Player
- fastForward-Methode Windows Media Player , Controls-Klasse
- Steuert die Windows Media Player , fastForward-Methode
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
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341816"
---
# <a name="controlsfastforward-method"></a>Controls.fastForward-Methode

Die **fastForward-Methode** startet die schnelle Wiedergabe des Medienelements in vorwärts gerichteter Richtung.

## <a name="syntax"></a>Syntax


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **fastForward-Methode** gibt den Clip mit der fünffachen Normalengeschwindigkeit wieder. Durch das Aufrufen **von fastForward** wird die *Einstellungen.* **rate-Eigenschaft** auf 5,0. Wenn **die** Rate anschließend geändert wird oder **wiedergabe** oder **stop** aufgerufen wird, Windows Media Player die schnelle Weiterleitung beendet.

Die **fastForward-Methode** funktioniert nicht für Liveübertragungen und bestimmte Medientypen. Rufen Sie **isAvailable**("FastForward") auf, um zu bestimmen, ob Sie in einem Clip schnell vorwärts gehen können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **fastForward verwendet,** um die schnelle Wiedergabe des Medienelements zu starten. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Einstellungen.rate**](settings-rate.md)
</dt> </dl>

 

 





