---
description: Dieser Operator überlädt den Zuweisungs Operator zum Kopieren eines Medientyps.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Cmediatype. cmediatype:: Operator =-Methode (mtype. h)-mtype-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389036"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>Cmediatype. cmediatype:: Operator =-Methode (mtype. h)

Dieser Operator überlädt den Zuweisungs Operator zum Kopieren eines Medientyps.

## <a name="syntax"></a>Syntax


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ atur\]
</dt> <dd>

Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das-Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




