---
description: Die BreakConnect-Methode gibt einen Pin von einer Verbindung frei.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: CTransformFilter.BreakConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053810"
---
# <a name="ctransformfilterbreakconnect-method"></a>CTransformFilter.BreakConnect-Methode

Die `BreakConnect` -Methode gibt einen Pin aus einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dir* 
</dt> <dd>

Member des [**PIN DIRECTION-Enumerationstyps, \_**](/windows/win32/api/strmif/ne-strmif-pin_direction) der angibt, welche Pinverbindung unterbrochen wurde (Eingabe oder Ausgabe).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Methoden [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) und [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) rufen diese Methode auf, wenn eine Pinverbindung unterbrochen wird. Diese Methode führt in der Basisklasse nichts aus. Wenn Sie die [**CheckConnect-Methode**](ctransformfilter-checkconnect.md) überschreiben, überschreiben Sie diese Methode, um alle in der **CheckConnect-Methode** abgerufenen Ressourcen freizugeben, einschließlich Schnittstellenzeigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




