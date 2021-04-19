---
description: Die TAPI-Zeile \_ appnewcallhub-Nachricht wird gesendet, um eine Anwendung zu informieren, wenn ein neuer callhub erstellt wurde.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: LINE_APPNEWCALLHUB Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369183"
---
# <a name="line_appnewcallhub-message"></a>Zeile \_ appnewcallhub-Nachricht

Die TAPI- **Zeile \_ appnewcallhub** -Nachricht wird gesendet, um eine Anwendung zu informieren, wenn ein neuer callhub erstellt wurde.


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

Die nach Verfolgungs Ebene für den neuen Hub, wie von einer der [**linecallhubtracking- \_ Konstanten**](linecallhubtracking--constants.md)definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht stammt von TAPI anstelle eines Dienstanbieters, sodass keine entsprechende TSPI-Nachricht vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




