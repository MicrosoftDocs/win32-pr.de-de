---
description: 'Die endflush-Methode beendet einen Löschvorgang. Implementiert die IPin:: endflush-Methode.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Cbaseiniputpin. endflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366943"
---
# <a name="cbaseinputpinendflush-method"></a>Cbaseiniputpin. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang. Implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt das [**\_ bgeleert-Flag "cbaseinputpin:: m**](cbaseinputpin-m-bflushing.md) " auf " **true**" fest, wodurch die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode Beispiele annehmen kann.

Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:

1.  Geben Sie alle gepufferten Daten frei, und warten Sie, bis alle Samples in der Warteschlange verworfen wurden
2.  Löschen Sie alle ausstehenden " [**EC \_ Complete**](ec-complete.md) "-Benachrichtigungen.
3.  Ruft die Methode der Basisklasse auf.
4.  Nennen Sie [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für nachgeschaltete Eingabe Pins. Wenn die PIN noch keine Medien Beispiele nach unten übermittelt hat, können Sie diesen Schritt überspringen. Wenn die Ausgabe Pins von der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet werden, können Sie die [**cbaseoutputpin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) -Methode aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




