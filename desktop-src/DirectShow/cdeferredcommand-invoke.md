---
description: Die Invoke-Methode ermöglicht den Zugriff auf Methoden und Eigenschaften, die von einem -Objekt verfügbar gemacht werden.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: CDeferredCommand.Invoke-Methode (Ctlutil.h)
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
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074374"
---
# <a name="cdeferredcommandinvoke-method"></a>CDeferredCommand.Invoke-Methode

Die `Invoke` -Methode ermöglicht den Zugriff auf Methoden und Eigenschaften, die von einem -Objekt verfügbar gemacht werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E \_ ALREADY CANCELLED \_ zurück, wenn m **\_ pQueue** **NULL ist.** Andernfalls gibt das **HRESULT zurück,** das sich aus einem Aufruf von **IDispatch::GetTypeInfo** oder **IUnknown::QueryInterface ergibt.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




