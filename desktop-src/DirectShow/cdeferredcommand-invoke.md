---
description: Die Aufruf Methode ermöglicht den Zugriff auf Methoden und Eigenschaften, die von einem-Objekt verfügbar gemacht werden.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Cdeferredcommand. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371180"
---
# <a name="cdeferredcommandinvoke-method"></a>Cdeferredcommand. aufrufen-Methode

Die- `Invoke` Methode bietet Zugriff auf Methoden und Eigenschaften, die von einem-Objekt verfügbar gemacht werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt VFW E zurück, die \_ \_ bereits \_ abgebrochen wurde, wenn **m \_ pqueue** **null** ist. Andernfalls wird das **HRESULT** zurückgegeben, das sich aus einem **IDispatch:: GetTypeInfo** -oder **IUnknown:: QueryInterface**-Ausdruck ergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




