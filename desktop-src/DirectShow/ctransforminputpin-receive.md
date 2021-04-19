---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode implementiert die IMemInputPin:: Receive-Methode.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Ctransforminputpin. Receive-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367192"
---
# <a name="ctransforminputpinreceive-method"></a>Ctransforminputpin. Receive-Methode

Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode implementiert die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.

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

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                        |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode der PIN auf, die den streamingzustand der PIN überprüft und auf Formatänderungen im Medientyp prüft. Anschließend wird die [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode des Filters aufgerufen, die das Beispiel verarbeitet und es nach unten übermittelt.

Wenn der Filter auf das Beispiel zugreifen muss, nachdem diese Methode zurückgegeben wurde, sollte Sie einen Verweis Zähler enthalten, indem die **IUnknown:: adressf** -Methode für das Beispiel aufgerufen wird. Beispielsweise benötigen einige Decoder-Filter das aktuelle Beispiel, um das nächste Beispiel zu decodieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




