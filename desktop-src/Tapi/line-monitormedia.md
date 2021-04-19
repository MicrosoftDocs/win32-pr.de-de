---
description: Die TAPI-LINE_MONITORMEDIA Nachricht wird gesendet, wenn eine Änderung im Medientyp "Aufrufe" erkannt wird. Das Senden dieser Nachricht wird mit der linemonitormedia-Funktion gesteuert.
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352972"
---
# <a name="line_monitormedia-message"></a>Zeile \_ monitormedia-Meldung

Die TAPI **- \_ Linien** Überwachung wird gesendet, wenn eine Änderung im Medientyp des Aufrufes erkannt wird. Das Senden dieser Nachricht wird mit der [**linemonitormedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) -Funktion gesteuert.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den-Befehl.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der neue Medientyp (oder-Modus). Dieser Parameter darf nur eine der [**linemediamode- \_ Konstanten**](linemediamode--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), an der das angegebene Medium erkannt wurde. Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ monitormedia** -Nachricht wird an die Anwendung gesendet, die die Medienüberwachung für den erkannten Medientyp aktiviert hat.

Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_ Monitor Ziffern**](line-monitordigits.md), Zeilen Überwachung) generierten Nachrichten [**nützlich \_**](line-monitortone.md), um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen. Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.

Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ gatherziffern**](line-gatherdigits.md)
</dt> <dt>

[**Zeilen \_ Generierung**](line-generate.md)
</dt> <dt>

[**Zeilen \_ monitorziffern**](line-monitordigits.md)
</dt> <dt>

[**\_linienmonitortone**](line-monitortone.md)
</dt> </dl>

 

 




