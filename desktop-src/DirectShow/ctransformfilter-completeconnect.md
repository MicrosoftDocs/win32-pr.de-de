---
description: 'CTransformFilter.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Pinverbindung ab.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: CTransformFilter.CompleteConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e708745231f320d143c55403a75178e78432a162c3c89fc2c5fe8fd62cdd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687310"
---
# <a name="ctransformfiltercompleteconnect-method"></a>CTransformFilter.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Pinverbindung ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*direction* 
</dt> <dd>

Member des [**PIN DIRECTION-Enumerationstyps, \_**](/windows/win32/api/strmif/ne-strmif-pin_direction) der angibt, welcher Pin auf dem Filter die Verbindung herstellen soll.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins in diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Methoden [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) und [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) rufen diese Methode während des Pinverbindungsprozesses auf. Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




