---
description: Die TAPI LINE APPNEWCALLHUB-Nachricht wird gesendet, um eine Anwendung zu \_ informieren, wenn ein neuer Call Hub erstellt wurde.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: LINE_APPNEWCALLHUB (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf413f16270ba54fd7447cc0c41c040759edd699c995eac79314b9961486ce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905903"
---
# <a name="line_appnewcallhub-message"></a>LINE \_ APPNEWCALLHUB-Nachricht

Die TAPI **LINE \_ APPNEWCALLHUB-Nachricht** wird gesendet, um eine Anwendung zu informieren, wenn ein neuer Call Hub erstellt wurde.


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

Die Rückrufinstanz, die beim Öffnen der Zeile des Aufrufs angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Die Nachverfolgungsebene auf dem neuen Hub, wie durch eine der [**LINECALLHUBTRACKING-Konstanten \_ definiert.**](linecallhubtracking--constants.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Nachricht stammt aus TAPI und nicht aus einem Dienstanbieter, sodass keine entsprechende TSPI-Nachricht angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




