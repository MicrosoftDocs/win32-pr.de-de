---
description: Die GetReader-Methode gibt einen Zeiger auf die IAsyncReader-Schnittstelle des Ausgabepins zurück.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: CPullPin.GetReader-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7880cba8e910c3da8ade049e18ae22e403c0c616246e4dfde94e587a1fcdeab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055000"
---
# <a name="cpullpingetreader-method"></a>CPullPin.GetReader-Methode

Die `GetReader` -Methode gibt einen Zeiger auf die [**IAsyncReader-Schnittstelle des Ausgabepins**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) zurück.

## <a name="syntax"></a>Syntax


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) zurück.

## <a name="remarks"></a>Hinweise

Die zurückgegebene Schnittstelle verfügt über eine ausstehende Verweisanzahl. Der Aufrufer muss die Schnittstelle frei geben.

Die -Methode überprüft den Wert des Schnittstellenzeigers nicht vor dem Aufruf von **AddRef.** Rufen Sie diesen daher erst auf, wenn Sie die [**CPullPin::Verbinden**](cpullpin-connect.md) aufgerufen haben. Andernfalls ist der Schnittstellenzeiger möglicherweise **NULL,** und der Aufruf **von AddRef** löst eine Ausnahme aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




