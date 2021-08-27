---
description: Die Next-Methode ruft eine angegebene Anzahl von Medientypen ab. Diese Methode implementiert die IEnumMediaTypes::Next-Methode.
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: CEnumMediaTypes.Next-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8dd593fe6ca550c55ffc1f769a303dd2d5cbf7a8d8c986be8a39278d7f334ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131290"
---
# <a name="cenummediatypesnext-method"></a>CEnumMediaTypes.Next-Methode

Die `Next` -Methode ruft eine angegebene Anzahl von Medientypen ab. Diese Methode implementiert die [**IEnumMediaTypes::Next-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next)

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Anzahl der abzurufenden Medientypen.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Array von Zeigern auf [**AM \_ MEDIA \_ TYPE-Strukturen**](/windows/win32/api/strmif/ns-strmif-am_media_type) der Größe *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der von der Methode zurückgegebenen Medientypen empfängt. Kann NULL **sein,** wenn *cMediaTypes* gleich 1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Es wurden nicht so viele Medientypen wie angefordert abgerufen.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Ungültiges Argument.<br/>                                                        |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>                  |  NULL-Zeigerargument.<br/>                                               |
| <dl> <dt>**VFW \_ \_ E-ENUM \_ NICHT \_ \_ SYNCHRON**</dt> </dl> | Der Zustand des Pins hat sich geändert und ist jetzt inkonsistent mit dem Enumerator.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich ist, enthält das von *ppMediaTypes* angegebene Array Zeiger auf AM \_ MEDIA \_ TYPE-Strukturen. Die Anzahl der Strukturen ist gleich *\* pcFetched.* Geben Sie jeden Medientyp frei, indem Sie die [**DeleteMediaType-Funktion**](deletemediatype.md) aufrufen.

Diese Methode ruft die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) des Pins auf, um die Medientypen abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CEnumMediaTypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




