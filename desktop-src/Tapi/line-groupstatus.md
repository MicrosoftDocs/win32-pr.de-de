---
description: Die Meldung "line \_ groupstatus" wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360409"
---
# <a name="line_groupstatus-message"></a>Zeilen \_ Gruppenstatus-Meldung

Die Meldung " **line \_ groupstatus** " wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.


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

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Gruppenstatus an, der geändert wurde. Die Anwendung kann [**linegetgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) aufrufen, um die Änderungen in verfügbaren Gruppen zu ermitteln. Der *dwParam2* -Parameter ist eine oder mehrere der [**linegroupstatus- \_ Konstanten**](linegroupstatus--constants.md).

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

[**linegetgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




