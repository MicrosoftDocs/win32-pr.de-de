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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085158"
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

## <a name="remarks"></a>Bemerkungen

Zu Beginn eines Leerungsvorgang ruft die [**CTransformInputPin::BeginFlush-Methode**](ctransforminputpin-beginflush.md) des Eingabepins diese Methode auf. Diese Methode übergibt den `BeginFlush` Aufruf downstream.

Wenn die abgeleitete Klasse einen Arbeitsthread verwendet, um Stichproben zu liefern, sollte sie alle Daten in der Warteschlange während eines Leerungsvorgang verwerfen. Dies kann entweder in der -Methode `BeginFlush` oder in der [**EndFlush-Methode**](ctransformfilter-endflush.md) erfolgen. Beachten Sie jedoch, dass Aufrufe `BeginFlush` von nicht mit dem Streamingthread synchronisiert werden. Wenn die -Methode die in der Warteschlange gespeicherten Daten verwirft, muss der Filter darauf achten, dass keine daten zwischen den Aufrufen und `BeginFlush` `BeginFlush` **EndFlush mehr verarbeiten.** Weitere Informationen finden Sie unter [Datenfluss für Filterentwickler.](data-flow-for-filter-developers.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




