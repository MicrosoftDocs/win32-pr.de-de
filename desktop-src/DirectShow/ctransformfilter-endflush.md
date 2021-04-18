---
description: Die endflush-Methode beendet einen Löschvorgang.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Ctransformfilter. endflush-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372402"
---
# <a name="ctransformfilterendflush-method"></a>Ctransformfilter. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Am Ende eines Leerungs Vorgangs ruft die [**ctransforminputpin:: endflush**](ctransforminputpin-endflush.md) -Methode der Eingabe-PIN diese Methode auf. Diese Methode übergibt den- `EndFlush` Rückruf.

Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Beispielen verwendet, muss Sie alle in der Warteschlange befindlichen Daten vor dem Senden des `EndFlush` Aufrufers verwerfen. Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




