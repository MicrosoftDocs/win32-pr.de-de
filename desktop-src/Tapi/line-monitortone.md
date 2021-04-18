---
description: Die TAPI- \_ linienmonitortone-Nachricht wird gesendet, wenn ein Ton erkannt wird. Das Senden dieser Nachricht wird mit der linemonitortones-Funktion gesteuert.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: LINE_MONITORTONE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358762"
---
# <a name="line_monitortone-message"></a>Zeile \_ monitortone-Meldung

Die TAPI **- \_ linienmonitortone** -Nachricht wird gesendet, wenn ein Ton erkannt wird. Das Senden dieser Nachricht wird mit der [**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) -Funktion gesteuert.


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

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der anwendungsspezifische **dwappspecific** -Member der [**linemonitortone**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) -Struktur für den erkannten Farbton.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der der Ton erkannt wurde. Bei API-Versionen vor 2,0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile " \_ monitortone** " wird nur an die Anwendung gesendet, die den überwachten Ton angefordert hat.

Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_ Monitor Ziffern**](line-monitordigits.md), Zeilen Überwachung) generierten Nachrichten **nützlich \_**, um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen. Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.

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

[**Linemonitortone**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




