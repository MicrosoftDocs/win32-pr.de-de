---
description: 'Die Next-Methode ruft eine angegebene Anzahl von Medientypen ab. Diese Methode implementiert die ienummediatypes:: Next-Methode.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Cenum mediatypes. Next-Methode (amfilter. h)
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
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361568"
---
# <a name="cenummediatypesnext-method"></a>Cenum mediatypes. Next-Methode

Die- `Next` Methode ruft eine angegebene Anzahl von Medientypen ab. Diese Methode implementiert die [**ienummediatypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) -Methode.

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

*cmediatypes* 
</dt> <dd>

Anzahl der abzurufenden Medientypen.

</dd> <dt>

*ppmediatypes* 
</dt> <dd>

Array von Zeigern auf die [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Strukturen der Größe von *cpins*.

</dd> <dt>

*pcfetch* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Medientypen empfängt, die von der Methode zurückgegeben wurden. Kann **null** sein, wenn *cmediatypes* den Wert 1 hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Es wurden nicht so viele Medientypen wie angefordert abgerufen.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>               | Ungültiges Argument.<br/>                                                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeigerargument.<br/>                                               |
| <dl> <dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt> </dl> | Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich ausgeführt wird, enthält das von *ppmediatypes* angegebene Array Zeiger \_ auf \_ Medientyp Strukturen. Die Anzahl der Strukturen ist gleich *\* pcfetch*. Geben Sie jeden Medientyp frei, indem Sie die Funktion [**deletemediatype**](deletemediatype.md) aufrufen.

Diese Methode ruft die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode der PIN auf, um die Medientypen abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenum mediatypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




