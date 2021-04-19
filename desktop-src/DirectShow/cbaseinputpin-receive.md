---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode implementiert die IMemInputPin:: Receive-Methode.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Cbasinput PIN. Receive-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369952"
---
# <a name="cbaseinputpinreceive-method"></a>Cbasinput PIN. Receive-Methode

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

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                             | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeigerargument.<br/>                      |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Ungültiger Medientyp.<br/>                             |
| <dl> <dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt> </dl>   | Laufzeitfehler.<br/>                      |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>     | Die PIN wurde beendet.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Die upstreamausgabepin ruft diese Methode auf, um ein Beispiel an die Eingabe-PIN zu übermitteln Die Eingabe-PIN muss eine der folgenden Aktionen ausführen:

-   Verarbeiten Sie das Beispiel vor der Rückgabe.
-   Geben Sie zurück, und verarbeiten Sie das Beispiel in einem Arbeits Thread.
-   Ablehnen Sie das Beispiel.

Wenn die PIN einen Arbeits Thread zum Verarbeiten des Beispiels verwendet, fügen Sie dem Beispiel innerhalb dieser Methode einen Verweis Zähler hinzu. Nachdem die Methode zurückgegeben wurde, gibt die upstreampin das Beispiel frei. Wenn der Verweis Zähler des Beispiels 0 (null) erreicht, wird das Beispiel zur erneuten Verwendung an die Zuweisung zurückgegeben.

Diese Methode ist synchron und kann blockiert werden. Wenn die-Methode blockiert werden kann, sollte die [**cbaseinputpin:: receivecanblock**](cbaseinputpin-receivecanblock.md) -Methode der PIN s OK zurückgeben \_ .

In der-Basisklasse führt diese Methode die folgenden Schritte aus:

1.  Ruft die [**cbaseinputpin:: checkstreaming**](cbaseinputpin-checkstreaming.md) -Methode auf, um zu überprüfen, ob die PIN jetzt Beispiele verarbeiten kann. Wenn die PIN beispielsweise nicht beendet wird, schlägt die Methode fehl.
2.  Ruft die Beispiel Eigenschaften ab und überprüft, ob sich das Format geändert hat (siehe unten).
3.  Wenn sich das Format geändert hat, ruft die-Methode die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu bestimmen, ob das neue Format zulässig ist.
4.  Wenn das neue Format nicht zulässig ist, ruft die-Methode die [**cbasepin:: EndOf Stream**](cbasepin-endofstream.md) -Methode auf, \_ gibt ein EC errorabort-Ereignis aus und gibt einen Fehlercode zurück.
5.  Wenn keine Fehler aufgetreten sind, gibt die Methode "S OK" zurück \_ .

Testen Sie die Formatänderung wie folgt:

-   Wenn das Beispiel die [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle unterstützt, überprüfen Sie den **dwsampleflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur. Wenn das "am \_ Sample Sample \_ typechanged"-Flag vorhanden ist, hat sich das Format geändert.
-   Wenn das Beispiel **IMediaSample2** nicht unterstützt, müssen Sie andernfalls die [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) -Methode aufrufen. Wenn die Methode einen nicht-**null** -Wert zurückgibt, hat sich das Format geändert.

In der-Basisklasse verarbeitet diese Methode das Beispiel nicht. Die abgeleitete Klasse muss diese Methode überschreiben, um die Verarbeitung auszuführen. (Was dies bedeutet, hängt vollständig vom Filter ab.) Die abgeleitete Klasse sollte die Basisklassen Methode abrufen, um die zuvor beschriebenen Fehler zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




