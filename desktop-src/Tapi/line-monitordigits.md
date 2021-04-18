---
description: Die TAPI- \_ linienmonitordigits-Nachricht wird gesendet, wenn eine Ziffer erkannt wird. Das Senden dieser Nachricht wird mit der linemonitordigits-Funktion gesteuert.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: LINE_MONITORDIGITS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368440"
---
# <a name="line_monitordigits-message"></a>Zeile " \_ monitordigits"-Meldung

Die TAPI **- \_ linienmonitordigits** -Nachricht wird gesendet, wenn eine Ziffer erkannt wird. Das Senden dieser Nachricht wird mit der [**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) -Funktion gesteuert.


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

Das nieder wertige Byte enthält die letzte in einer Textdarstellung empfangene Ziffer.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Ziffern Modus, der erkannt wurde. Dieser Parameter darf nur eine der [**linedigitmode- \_ Konstanten**](linedigitmode--constants.md)sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der die angegebene Ziffer erkannt wurde. Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Meldung **Zeile \_ monitordigits** wird an die Anwendung gesendet, in der die Ziffern Überwachung aktiviert ist.

Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_**](line-monitormedia.md)Überwachung, Zeilen Überwachung) generierten Nachrichten nützlich, um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen. [**\_**](line-monitortone.md) Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.

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

[**Zeilen- \_ monitormedia**](line-monitormedia.md)
</dt> <dt>

[**\_linienmonitortone**](line-monitortone.md)
</dt> <dt>

[**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




