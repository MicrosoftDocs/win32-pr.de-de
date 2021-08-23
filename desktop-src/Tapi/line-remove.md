---
description: Die TAPI LINE REMOVE-Meldung wird gesendet, um eine Anwendung über das Entfernen (Löschen aus dem \_ System) eines Liniengeräts zu informieren.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: LINE_REMOVE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13f36123cb8cb77bd2d4b78c3e69a2da1c027aef4dad1fc9dfd7f3c6a00399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335920"
---
# <a name="line_remove-message"></a>LINE \_ REMOVE-Meldung

Die TAPI **LINE \_ REMOVE-Meldung** wird gesendet, um eine Anwendung über das Entfernen (Löschen aus dem System) eines Liniengeräts zu informieren. Im Allgemeinen wird dies nicht für vorübergehende Entfernungen verwendet, z. B. für die Extraktion von PCMCIA-Geräten, sondern nur für dauerhafte Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert würde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Bezeichner des Zeilengeräts, das entfernt wurde.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Anwendungen, die TAPI Version 2.0 oder höher unterstützen, erhalten eine **LINE \_ REMOVE-Meldung.** Dadurch werden sie darüber informiert, dass das Gerät aus dem System entfernt wurde. Der **LINE \_ REMOVE-Meldung** wird auf jedem Zeilenhand handle eine [**LINE \_ CLOSE-Meldung**](line-close.md) voranstehen, wenn die Anwendung die Zeile geöffnet hat. Diese Meldung wird an alle Anwendungen gesendet, die TAPI Version 2.0 oder höher unterstützen und [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich anwendungen, für die zu diesem Zeitpunkt keine Liniengeräte geöffnet sind.

Älteren Anwendungen wird eine [**LINE \_ LINEDEVSTATE-Meldung**](line-linedevstate.md) gesendet, die LINEDEVSTATE REMOVED an, gefolgt \_ von einer LINE \_ CLOSE-Meldung. Im Gegensatz **zur LINE \_ REMOVE-Meldung** können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn die Zeile geöffnet ist, wenn sie entfernt wird. Wenn die Leitung nicht geöffnet ist, würde der einzige Hinweis darauf, dass das Gerät entfernt wurde, beim Versuch, auf das Gerät zu zugreifen, ein LINEERR \_ NODEVICE-Fehler angezeigt.

Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Geräte-ID auf das Gerät zu zugreifen, zu einem LINEERR \_ NODEVICE-Fehler. Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, belegt das entfernte Gerät keine Geräte-ID mehr.

> [!Note]  
> Implementierung: TapI gibt diese LINEERR NODEVICE zurück. Nachdem eine \_ **LINE \_ REMOVE-Nachricht** von einem Dienstanbieter empfangen wurde, werden keine weiteren Aufrufe an diesen Dienstanbieter mithilfe dieser Zeilengeräte-ID ausgeführt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




