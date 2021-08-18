---
description: 'CTransformFilter.BeginFlush-Methode: Die BeginFlush-Methode startet einen Leerungsvorgang.'
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: CTransformFilter.BeginFlush-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be20231cf62148e3487aef405735f764bf5c02b7cbaadba3c140728b66bd5391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053860"
---
# <a name="ctransformfilterbeginflush-method"></a>CTransformFilter.BeginFlush-Methode

Die `BeginFlush` -Methode startet einen Leerungsvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Zu Beginn eines Leerungsvorgangs ruft die [**CTransformInputPin::BeginFlush-Methode**](ctransforminputpin-beginflush.md) des Eingabepins diese Methode auf. Diese Methode übergibt den `BeginFlush` Aufruf downstream.

Wenn die abgeleitete Klasse einen Arbeitsthread zum Übermitteln von Beispielen verwendet, sollte sie während eines Leerungsvorgangs alle daten in der Warteschlange verwerfen. Dies kann entweder in der `BeginFlush` -Methode oder in der [**EndFlush-Methode**](ctransformfilter-endflush.md) erfolgen. Beachten Sie jedoch, dass Aufrufe von `BeginFlush` nicht mit dem Streamingthread synchronisiert werden. Wenn die `BeginFlush` -Methode die in der Warteschlange enthaltenen Daten verwirft, muss der Filter darauf achten, keine weiteren Daten zwischen dem - und dem `BeginFlush` **EndFlush-Aufruf** zu verarbeiten. Weitere Informationen finden Sie unter [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




