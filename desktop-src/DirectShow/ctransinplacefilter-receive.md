---
description: Die Receive-Methode empfängt ein Medienbeispiel, verarbeitet es und übermittelt es an den Downstreamfilter.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: CTransInPlaceFilter.Receive-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390d0243631e4ac31da779ca01197500f1d3df18127a3b86f0cf1ea834283f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053460"
---
# <a name="ctransinplacefilterreceive-method"></a>CTransInPlaceFilter.Receive-Methode

Die `Receive` -Methode empfängt ein Medienbeispiel, verarbeitet es und übermittelt es an den Downstreamfilter.

## <a name="syntax"></a>Syntax


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) im Beispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                  | Beschreibung                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler<br/> |



 

## <a name="remarks"></a>Hinweise

Der Eingabepin des Filters ruft diese Methode auf, wenn er ein Beispiel empfängt. Der Filter ruft die [**Transform-Methode**](ctransinplacefilter-transform.md) auf, die die abgeleitete Klasse implementieren muss. Die **Transform-Methode** verarbeitet die Daten. Wenn der Filter nur eine Zuweisung verwendet, übergibt er *pSample* direkt an die **Transform-Methode.** Andernfalls wird *pSample* kopiert und die Kopie übergeben.

Wenn die **Transform-Methode** S \_ FALSE zurückgibt, löscht die Methode das `Receive` Beispiel. Im ersten gelöschten Beispiel sendet der Filter ein [**EC \_ QUALITY \_ CHANGE-Ereignis**](ec-quality-change.md) an den Filtergraph-Manager. Andernfalls liefert der Filter das Ausgabebeispiel, wenn die **Transform-Methode** S OK \_ zurückgibt. Dazu ruft sie die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) auf dem Downstreameingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




