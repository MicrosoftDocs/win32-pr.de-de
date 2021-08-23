---
description: Die TAPI-LINE_MONITORMEDIA Nachricht wird gesendet, wenn eine Änderung des Aufrufmedientyps erkannt wird. Das Senden dieser Nachricht wird mit der lineMonitorMedia-Funktion gesteuert.
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fec42f0e8aa630b518f989a9237762edc71281767b281f7af78eb54210138d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519020"
---
# <a name="line_monitormedia-message"></a>LINE \_ MONITORMEDIA-Meldung

Die TAPI **LINE \_ MONITORMEDIA-Nachricht** wird gesendet, wenn eine Änderung des Medientyps des Aufrufs erkannt wird. Das Senden dieser Nachricht wird mit der [**lineMonitorMedia-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) gesteuert.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für den Aufruf.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der neue Medientyp (oder Modus). Dieser Parameter darf nur eine der [**LINEMEDIAMODE-Konstanten \_ sein.**](linemediamode--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Tickanzahl" (Anzahl von Millisekunden seit dem Start Windows), bei der das angegebene Medium erkannt wurde. Bei TAPI-Versionen vor 2.0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ MONITORMEDIA-Nachricht** wird an die Anwendung gesendet, die die Medienüberwachung für den erkannten Medientyp aktiviert hat.

Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem Computer generiert wurde, auf dem die Anwendung ausgeführt wird, ist er nur für den Vergleich mit anderen ähnlichen Nachrichten mit Zeitstempeln nützlich, die auf demselben Zeilengerät generiert wurden ( [**LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), um deren relative Zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen. Die Tickanzahl kann nach ungefähr 49,7 Tagen "umschließen". -Anwendungen müssen dies beim Ausführen von Berechnungen berücksichtigen.

Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. B. wenn er mit einer früheren Version von TAPI erstellt wurde), stellt TAPI einen Zeitstempel an dem Punkt bereit, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der synthetisierte Zeitstempel so genau wie möglich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**LINE \_ GENERATE**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




