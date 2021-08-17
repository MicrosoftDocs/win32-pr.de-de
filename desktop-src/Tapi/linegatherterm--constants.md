---
description: Die \_ LINEGATHERTERM-Bitflagkonstante beschreiben die Bedingungen, unter denen die Pufferziffernsammlung beendet wird.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: LINEGATHERTERM_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a6d5952ac4f69d11fd499df63554d6fda7dca76e46e4aad1a01ae326f363a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140033"
---
# <a name="linegatherterm_-constants"></a>\_LINEGATHERTERM-Konstanten

Die **\_ LINEGATHERTERM-Bitflagkonstante** beschreiben die Bedingungen, unter denen die Pufferziffernsammlung beendet wird.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



Die angeforderte Anzahl von Ziffern wurde erfasst. Der Puffer ist voll.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ CANCEL**
</dt> <dd> <dl> <dt>



Die Anforderung wurde von dieser Anwendung, von einer anderen Anwendung oder weil der Aufruf beendet wurde, abgebrochen.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



Das Timeout der ersten Ziffer ist abgelaufen. Der Puffer enthält keine Ziffern.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERTIMEOUT**
</dt> <dd> <dl> <dt>



Das ziffernübergreifende Timeout ist abgelaufen. Der Puffer enthält mindestens eine Ziffer.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



Eine der Beendigungsziffern passte zu einer empfangenen Ziffer. Die übereinstimmende Beendigungsziffer ist die letzte Ziffer im Puffer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




