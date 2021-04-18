---
description: 'Die cbaseinputpin-Methode startet einen Löschvorgang. Diese Methode implementiert die IPin:: beginflush-Methode.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Cbaseiniputpin. beginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357674"
---
# <a name="cbaseinputpinbeginflush-method"></a>Cbaseiniputpin. beginflush-Methode

Die- `CBaseInputPin` Methode startet einen Löschvorgang. Diese Methode implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt das [**\_ bgeleert-Flag "cbaseinputpin:: m**](cbaseinputpin-m-bflushing.md) " auf " **true**" fest. Dies bewirkt, dass die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode weitere Beispiele ablehnt.

Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:

1.  Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für nachgeschaltete Eingabe Pins. Wenn die PIN noch keine Medien Beispiele nach unten übermittelt hat, können Sie diesen Schritt überspringen. Wenn die Ausgabe Pins von der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet werden, können Sie die [**cbaseoutputpin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) -Methode aufrufen.
2.  Ruft die Methode der Basisklasse auf.
3.  Mit dem Verwerfen von Daten in der Warteschlange beginnen.
4.  Rückgabe von blockierten Aufrufen der **Receive** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




