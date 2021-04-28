---
description: 'CTransformFilter.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: CTransformFilter.EndFlush-Methode (Transfrm.h)
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
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085059"
---
# <a name="ctransformfilterendflush-method"></a>CTransformFilter.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Am Ende eines Leerungsvorgang ruft die [**CTransformInputPin::EndFlush-Methode**](ctransforminputpin-endflush.md) des Eingabepins diese Methode auf. Diese Methode übergibt den `EndFlush` Aufruf downstream.

Wenn die abgeleitete Klasse einen Arbeitsthread zum Senden von Beispielen verwendet, muss sie alle Daten in der Warteschlange verwerfen, bevor der Aufruf `EndFlush` nachgeschaltet wird. Weitere Informationen finden Sie unter [Datenfluss für Filterentwickler.](data-flow-for-filter-developers.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




