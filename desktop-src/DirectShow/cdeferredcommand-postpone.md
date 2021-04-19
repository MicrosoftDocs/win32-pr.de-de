---
description: Die Methode zum Verschieben gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Cdeferredcommand. Verschiebungen-Methode (ctlutil. h)
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
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374031"
---
# <a name="cdeferredcommandpostpone-method"></a>Cdeferredcommand. Verschiebungen-Methode

Die- `Postpone` Methode gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Neuzeit* 
</dt> <dd>

Neue Präsentationszeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine VFW E-Zeit zurück, die \_ \_ \_ bereits \_ vergangen ist, wenn *newTime* bereits vergangen ist Andernfalls wird ein **HRESULT** zurückgegeben, das sich aus einem Aufruf von [**ccmdqueue:: Remove**](ccmdqueue-remove.md) (beim Extrahieren aus der Liste) oder [**ccmdqueue:: Insert**](ccmdqueue-insert.md) ergibt (beim erneuten Verwenden der geänderten Zeit).

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ideferredcommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




