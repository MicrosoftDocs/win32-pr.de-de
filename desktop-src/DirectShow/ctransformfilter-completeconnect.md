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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095168"
---
# <a name="ctransformfiltercompleteconnect-method"></a>CTransformFilter.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Stecknadelverbindung ab.

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

Member des [**aufzählten PIN \_ DIRECTION-Typs,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der an gibt, welcher Pin im Filter die Verbindung hergestellt wird.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins in diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**Methoden CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) und [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) rufen diese Methode während des Pinverbindungsprozesses auf. Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




