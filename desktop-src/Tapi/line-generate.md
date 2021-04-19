---
description: Die TAPI-Zeile \_ zum Generieren der Nachricht wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern-oder Tongenerierung beendet wurde.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: LINE_GENERATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361381"
---
# <a name="line_generate-message"></a>Zeile \_ generieren (Meldung)

Die TAPI- **Zeile zum \_ generieren** der Nachricht wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern-oder Tongenerierung beendet wurde. Es kann immer nur eine solche Generierungs Anforderung für einen bestimmten Aufruf ausgeführt werden. Diese Meldung wird auch gesendet, wenn die Ziffern-oder Tongenerierung abgebrochen wird.


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

Der Grund, warum die Ziffern-oder Tongenerierung beendet wurde. Dieser Parameter darf nur eine der [**linegenerateterm- \_ Konstanten**](linegenerateterm--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), zu der die Ziffern-oder Tongenerierung abgeschlossen wurde. Bei API-Versionen vor 2,0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile Nachricht \_ generieren** wird nur an die Anwendung gesendet, die die Ziffern-oder Tongenerierung angefordert hat.

Da der durch *dwParam3* angegebene Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für den Vergleich mit anderen gleichzeitig auf demselben Zeilen Medium ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ monitorziffern**](line-monitordigits.md), [**line \_ monitormedia**](line-monitormedia.md), [**line \_ monitortone**](line-monitortone.md)) generierten Zeitstempel nützlich. Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.

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

[**Zeilen \_ monitorziffern**](line-monitordigits.md)
</dt> <dt>

[**Zeilen- \_ monitormedia**](line-monitormedia.md)
</dt> <dt>

[**\_linienmonitortone**](line-monitortone.md)
</dt> </dl>

 

 




