---
description: Die beginflush-Methode startet einen Löschvorgang.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Ctransformfilter. beginflush-Methode (Transfrm. h)
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
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373662"
---
# <a name="ctransformfilterbeginflush-method"></a>Ctransformfilter. beginflush-Methode

Die- `BeginFlush` Methode startet einen Löschvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Zu Beginn eines Leerungs Vorgangs ruft die [**ctransforminputpin:: beginflush**](ctransforminputpin-beginflush.md) -Methode der Eingabe-PIN diese Methode auf. Diese Methode übergibt den- `BeginFlush` Rückruf.

Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Beispielen verwendet, sollte Sie alle in der Warteschlange befindlichen Daten während eines Löschvorgangs verwerfen. Dies kann entweder in der- `BeginFlush` Methode oder in der [**endflush**](ctransformfilter-endflush.md) -Methode erfolgen. Beachten Sie jedoch, dass Aufrufe von `BeginFlush` nicht mit dem streamingthread synchronisiert werden. Wenn die `BeginFlush` -Methode die in der Warteschlange befindlichen Daten verwirft, muss der Filter darauf achten, dass keine weiteren Daten zwischen den `BeginFlush` -und **endflush** -aufrufen verarbeitet werden. Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




