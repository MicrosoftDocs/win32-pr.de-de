---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Ctransformfilter. checkConnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370597"
---
# <a name="ctransformfiltercheckconnect-method"></a>Ctransformfilter. checkConnect-Methode

Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dir* 
</dt> <dd>

Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.

</dd> <dt>

*ppin* 
</dt> <dd>

Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: checkConnect**](ctransforminputpin-checkconnect.md) -Methode und die [**ctransformoutputpin:: checkConnect**](ctransformoutputpin-checkconnect.md) -Methode ruft diese Methode während des PIN-Verbindungsprozesses auf. Diese Methode führt in der Basisklasse keine Aktion aus. Diese kann von der abgeleiteten Klasse überschrieben werden. Beispielsweise kann die abgeleitete Klasse die andere PIN für eine bestimmte Schnittstelle Abfragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




