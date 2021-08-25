---
description: Die TAPI LINE DEVSPECIFICEX-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem \_ Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: LINE_DEVSPECIFICEX (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867070"
---
# <a name="line_devspecificex-message"></a>LINE \_ DEVSPECIFICEX-Meldung

Die TAPI **LINE \_ DEVSPECIFICEX-Nachricht** wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für ein Liniengerät oder einen Anruf. Dieser Parameter ist gerätespezifisch.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gerätespezifisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ DEVSPECIFICEX-Nachricht** wird von einem Dienstanbieter in Verbindung mit der [**lineDevSpecific-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) verwendet. Seine Bedeutung ist gerätespezifisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




