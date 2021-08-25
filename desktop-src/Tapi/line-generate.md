---
description: Die TAPI LINE GENERATE-Meldung wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern- oder \_ Tongenerierung beendet wurde.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: LINE_GENERATE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3ab0d503d7515fec2cdbd1676eed235cced88e2adfa9fcc1dd354663929e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774240"
---
# <a name="line_generate-message"></a>LINE \_ GENERATE-Nachricht

Die TAPI **LINE \_ GENERATE-Meldung** wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern- oder Tongenerierung beendet wurde. Es kann immer nur eine solche Generierungsanforderung für einen bestimmten Aufruf in Bearbeitung sein. Diese Meldung wird auch gesendet, wenn die Ziffern- oder Tongenerierung abgebrochen wird.


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

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Grund, warum die Ziffern- oder Tongenerierung beendet wurde. Dieser Parameter muss eine und nur eine der [**LINEGENERATETERM-Konstanten \_ sein.**](linegenerateterm--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die "Tickanzahl" (Anzahl von Millisekunden seit Windows gestartet), bei der die Ziffern- oder Tongenerierung abgeschlossen wurde. Bei API-Versionen vor 2.0 wird dieser Parameter nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ GENERATE-Nachricht** wird nur an die Anwendung gesendet, die die Ziffern- oder Tongenerierung angefordert hat.

Da der von *dwParam3* angegebene Zeitstempel möglicherweise auf einem anderen Computer als dem generiert wurde, auf dem die Anwendung ausgeführt wird, ist er nur für den Vergleich mit anderen ähnlich zeitstempelierten Nachrichten nützlich, die auf demselben Zeilengerät generiert wurden [**(LINE \_ GATHERDIGITS,**](line-gatherdigits.md) [**LINE \_ MONITORDIGITS,**](line-monitordigits.md) [**LINE \_ MONITORMEDIA,**](line-monitormedia.md) [**LINE \_ MONITORTONE),**](line-monitortone.md)um deren relative Zeitsteuerung (Trennung zwischen Ereignissen) zu bestimmen. Die Tickanzahl kann nach ungefähr 49,7 Tagen "umschließen". -Anwendungen müssen dies beim Ausführen von Berechnungen berücksichtigen.

Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. B. wenn er mit einer früheren Version von TAPI erstellt wurde), stellt TAPI einen Zeitstempel an dem Punkt zur Verfügung, der dem Dienstanbieter am nächsten ist, der das Ereignis generiert, sodass der synthetisierte Zeitstempel so genau wie möglich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




