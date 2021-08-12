---
title: Controls.fastReverse-Methode
description: Die fastReverse-Methode beginnt mit dem schnellen Scannen des Medienelements in umgekehrter Richtung.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- fastReverse-Methode Windows Media Player
- fastReverse-Methode Windows Media Player , Controls-Klasse
- Steuert die Klasse Windows Media Player , fastReverse-Methode
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4643525f66102cbd7b017a4a48f1068489062ec0849f197f1f55df45fc6f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580276"
---
# <a name="controlsfastreverse-method"></a>Controls.fastReverse-Methode

Die **fastReverse-Methode** beginnt mit dem schnellen Scannen des Medienelements in umgekehrter Richtung.

## <a name="syntax"></a>Syntax


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **fastReverse-Methode** scannt den Clip um das Fünffache der Normalgeschwindigkeit in umgekehrter Richtung und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt. Durch den Aufruf von **fastReverse** wird die *Einstellungen* geändert. **rate-Eigenschaft** auf 5,0. Wenn **die Rate** anschließend geändert wird oder **Wiedergabe** oder **Beendigung** aufgerufen wird, wird Windows Media Player schnell in umgekehrter Richtung beendet.

Wenn das Element Teil einer Wiedergabeliste ist, wird **fastReverse** am Anfang der aktuellen Spur angehalten. Wenn z. B. Track 3 sich in **fastReverse** befindet, wenn der Anfang von Track 3 erreicht ist, wird Windows Media Player nicht zu Track 2 wechseln. Die Wiedergabeanzahl wird beim Aufrufen von **fastReverse** nicht erhöht.

Wenn Sie **fastForward** aufrufen, während **fastReverse** wirksam ist, wird **fastReverse** beendet, und **fastForward** beginnt.

Diese Methode funktioniert nicht für Liveübertragungen und bestimmte Medientypen. Rufen Sie **isAvailable**("FastReverse") auf, um zu bestimmen, ob Sie schnelles Reverse in einem Clip verwenden können.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **fastReverse** verwendet, um die schnelle umgekehrte Wiedergabe des Medienelements zu starten. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Einstellungen.rate**](settings-rate.md)
</dt> </dl>

 

 





