---
description: Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und übergibt sie an den downstreamfilter.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Ctransinplacefilter. Receive-Methode (transip. h)
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
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366822"
---
# <a name="ctransinplacefilterreceive-method"></a>Ctransinplacefilter. Receive-Methode

Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und übergibt sie an den downstreamfilter.

## <a name="syntax"></a>Syntax


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle im Beispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                  | Beschreibung                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>          |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie ein Beispiel empfängt. Der Filter Ruft die [**Transformations**](ctransinplacefilter-transform.md) Methode auf, die von der abgeleiteten Klasse implementiert werden muss. Die **Transformations** Methode verarbeitet die Daten. Wenn der Filter nur einen Zuweiser verwendet, übergibt er *psample* direkt an die **Transformations** Methode. Andernfalls kopiert Sie *psample* und übergibt die Kopie.

Wenn die **Transform** -Methode S \_ false zurückgibt, löscht die- `Receive` Methode das Beispiel. Im ersten gelöschten Beispiel sendet der Filter ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager. Andernfalls liefert der  \_ Filter das Ausgabe Beispiel, wenn die Transform-Methode "S OK" zurückgibt. Zu diesem Zweck wird die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die downstreameingabepin aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




