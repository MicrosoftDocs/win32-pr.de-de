---
description: Die TAPI LINE CLOSE-Meldung wird gesendet, wenn das angegebene Zeilengerät \_ gesperrt wurde. Das Zeilengerätehandles oder alle Aufrufhandles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68fec993987bfc3ca36099d90eed2beadde9a749f965a36ebb6c513c210f387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682400"
---
# <a name="line_close-message"></a>LINE \_ CLOSE-Meldung

Die TAPI **LINE \_ CLOSE-Meldung** wird gesendet, wenn das angegebene Zeilengerät gesperrt wurde. Das Zeilengerätehandles oder alle Aufrufhandles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für das geschlossene Liniengerät. Dieses Handle ist nicht mehr gültig.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ CLOSE-Nachricht** wird erst an eine beliebige Anwendung gesendet, nachdem der TAPI-Dienstanbieter (TSP) eine offene Zeile geschlossen hat. Ob die Zeile unmittelbar nach einem erzwungenen Schließen erneut geöffnet werden kann, ist gerätespezifisch.

Die verursachende Bedingung kann eine erhebliche Zustandsänderung, ein Hardwarefehler, ein Verlust der Verbindung mit einem Server oder sogar eine potenzielle Verhinderung sein, dass eine einzelne Anwendung ein Liniengerät zu lange überbeschleunigen kann. Ein Liniengerät kann auch gesperrt werden, nachdem der Benutzer die Konfiguration dieser Zeile oder seines Treibers geändert hat. Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Systemneustart), und sie sich auf die aktuelle Ansicht des Geräts der Anwendung auswirken (z. B. eine Änderung der Gerätefunktionen), kann ein Dienstanbieter das Zeilengerät ersingen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




