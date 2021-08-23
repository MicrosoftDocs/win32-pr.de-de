---
description: Die Postpone-Methode gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: CDeferredCommand.Postpone-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074364"
---
# <a name="cdeferredcommandpostpone-method"></a>CDeferredCommand.Postpone-Methode

Die `Postpone` -Methode gibt eine neue Präsentationszeit für einen zuvor in der Warteschlange stehenden Befehl an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newtime* 
</dt> <dd>

Neue Präsentationszeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E TIME ALREADY PASSED \_ \_ \_ zurück, wenn *newtime* bereits übergeben wurde. Andernfalls gibt ein **HRESULT** zurück, das aus einem Aufruf von [**CCmdQueue::Remove**](ccmdqueue-remove.md) (beim Extrahieren aus der Liste) oder [**CCmdQueue::Insert**](ccmdqueue-insert.md) (beim erneuten Einfügen mit der geänderten Zeit) resultiert.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IDeferredCommand::P ostpone-Methode.**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




