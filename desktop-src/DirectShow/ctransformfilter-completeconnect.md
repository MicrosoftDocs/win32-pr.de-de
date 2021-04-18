---
description: Die completeconnect-Methode schließt eine PIN-Verbindung ab.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Ctransformfilter. completeconnect-Methode (Transfrm. h)
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
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357724"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Ctransformfilter. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine PIN-Verbindung ab.

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

Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.

</dd> <dt>

*preceivepin* 
</dt> <dd>

Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: completeconnect**](ctransforminputpin-completeconnect.md) -Methode und die [**ctransformoutputpin:: completeconnect**](ctransformoutputpin-completeconnect.md) -Methode ruft diese Methode während des PIN-Verbindungsprozesses auf. Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




