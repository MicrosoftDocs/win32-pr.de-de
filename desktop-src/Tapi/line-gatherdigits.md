---
description: Die TAPI \_ -Line gatherdigits-Nachricht wird gesendet, wenn die aktuelle gepufferte Digit-Sammlungs Anforderung beendet oder abgebrochen wurde. Der Ziffern Puffer kann überprüft werden, nachdem diese Nachricht von der Anwendung empfangen wurde.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: LINE_GATHERDIGITS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358060"
---
# <a name="line_gatherdigits-message"></a>Zeile \_ gatherdigits-Meldung

Die TAPI- **line \_ gatherdigits** -Nachricht wird gesendet, wenn die aktuelle gepufferte Digit-Sammlungs Anforderung beendet oder abgebrochen wurde. Der Ziffern Puffer kann überprüft werden, nachdem diese Nachricht von der Anwendung empfangen wurde.


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

Der Grund, warum die Ziffern Erfassung beendet wurde. Dieser Parameter darf nur eine der [**linegatherterm- \_ Konstanten**](linegatherterm--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der die Ziffern Erfassung abgeschlossen wurde. Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Meldung " **line \_ gatherdigits** " wird nur an die Anwendung gesendet, die die Ziffern Erfassung für den-Befehl mithilfe von [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)initiiert hat.

Wenn die [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) -Funktion verwendet wird, um eine vorherige Anforderung zum Erfassen von Ziffern abzubrechen, sendet TAPI eine **Zeile \_ gatherdigits** -Nachricht, bei der *dwParam1* auf linegatherterm Abbrechen festgelegt ist, \_ um anzugeben, dass der ursprünglich angegebene Puffer die Ziffern enthält, die für den Abbruch erfasst wurden.

Da der durch *dwParam3* angegebene Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen auf demselben Zeilen Gerät ( [**Zeilen \_ Generierung**](line-generate.md), Zeilen Überwachung, [**Zeilen \_**](line-monitormedia.md)Überwachung, Zeilen Überwachung) generierten Nachrichten nützlich, um deren relative zeitliche Steuerung (Trennung zwischen [**Ereignissen) \_ zu**](line-monitortone.md)bestimmen. [**\_**](line-monitordigits.md) Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.

Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.

> [!Note]  
> Wenn eine Anwendung einen asynchronen Vorgang aufruft, mit dem Daten in den Anwendungs Speicher geschrieben werden, muss die Anwendung diesen Arbeitsspeicher für das Schreiben verfügbar halten, bis eine [**Zeilen \_ Antwort**](line-reply.md) oder eine **Zeile \_ gatherdigits** -Nachricht empfangen wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ Generierung**](line-generate.md)
</dt> <dt>

[**Zeilen \_ monitorziffern**](line-monitordigits.md)
</dt> <dt>

[**Zeilen- \_ monitormedia**](line-monitormedia.md)
</dt> <dt>

[**\_linienmonitortone**](line-monitortone.md)
</dt> <dt>

[**Zeilen \_ Antwort**](line-reply.md)
</dt> <dt>

[**linegather-Ziffern**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




