---
title: Controls. fastreverse-Methode
description: Die fastreverse-Methode startet die schnelle Überprüfung des Medien Elements in umgekehrter Richtung.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- fastreverse-Methode, Windows-Media Player
- fastreverse-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, fastreverse-Methode
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
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370049"
---
# <a name="controlsfastreverse-method"></a>Controls. fastreverse-Methode

Die **fastreverse** -Methode startet die schnelle Überprüfung des Medien Elements in umgekehrter Richtung.

## <a name="syntax"></a>Syntax


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **fastreverse** -Methode scannt den Clip in umgekehrter Reihenfolge mit dem fünfmal normalen Tempo und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt. Durch Aufrufen von **fastreverse** werden die *Einstellungen* geändert. **bewerten** Sie die-Eigenschaft auf 5,0. Wenn die **Rate** anschließend geändert wird **oder wenn "** wiedergeben" oder " **Beenden** " aufgerufen wird, wird Windows Media Player schnell umkehren.

Wenn das Element Teil einer Wiedergabeliste ist, wird **fastreverse** am Anfang der aktuellen Spur angehalten. Wenn sich beispielsweise Track 3 in **fastreverse** befindet und der Anfang von Track 3 erreicht wird, wechselt Windows Media Player nicht mehr zu Track 2. Die Wiedergabe Anzahl wird beim Aufrufen von **fastreverse** nicht inkrementiert.

Wenn Sie **FastForward** aufzurufen, während **fastreverse** wirksam ist, wird **fastreverse** angehalten, und **FastForward** wird begonnen.

Diese Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen. Um zu ermitteln, ob Sie fast Reverse in einem Clip verwenden können, nennen Sie **IsAvailable**("fastreverse").

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **fastreverse** verwendet, um den schnellen umgekehrten Wiedergabe des Medien Elements zu starten. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls. FastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Pause**](controls-stop.md)
</dt> <dt>

[**"Settings. Rate"**](settings-rate.md)
</dt> </dl>

 

 





