---
description: Die Zeile \_ QueueStatus-Nachricht wird gesendet, wenn sich der Status einer ACD in der Warteschlange auf einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368457"
---
# <a name="line_queuestatus-message"></a>Zeile \_ QueueStatus-Meldung

Die **Zeile \_ QueueStatus** -Nachricht wird gesendet, wenn sich der Status einer ACD in der Warteschlange auf einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät. Dies bezieht sich auf den-Agent-Handler.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Bezeichner der Warteschlange, deren Status sich geändert hat.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Status der Warteschlange an, der geändert wurde. Kann eine oder mehrere der [**linequeuestatus- \_ Konstanten**](linequeuestatus--constants.md)sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




