---
description: 'CBaseInputPin.Receive-Methode: Die Receive-Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die IMemInputPin::Receive-Methode.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: CBaseInputPin.Receive-Methode (Amfilter.h)
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
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099688"
---
# <a name="cbaseinputpinreceive-method"></a>CBaseInputPin.Receive-Methode

Die `Receive` -Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die [**IMemInputPin::Receive-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

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

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                             | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Pin wird gerade geleert. Das Beispiel wurde abgelehnt.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>               |  NULL-Zeigerargument.<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Ungültiger Medientyp.<br/>                             |
| <dl> <dt>**VFW \_ \_ E-LAUFZEITFEHLER \_**</dt> </dl>   | Laufzeitfehler.<br/>                      |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl>     | Die Stecknadel wird beendet.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Der Upstreamausgabepin ruft diese Methode auf, um ein Beispiel an den Eingabepin zu übermitteln. Der Eingabepin muss einen der folgenden Schritte ausführen:

-   Verarbeiten Sie das Beispiel vor der Rückgabe.
-   Gibt zurück und verarbeitet das Beispiel in einem Arbeitsthread.
-   Lehnt das Beispiel ab.

Wenn der Pin einen Arbeitsthread zum Verarbeiten des Beispiels verwendet, fügen Sie dem Beispiel innerhalb dieser Methode einen Verweiszähler hinzu. Nachdem die Methode zurückgegeben wurde, gibt der Upstream-Pin das Beispiel frei. Wenn der Verweiszähler der Stichprobe 0 (null) erreicht, kehrt das Beispiel zur erneuten Verwendung zur Zuweisung zurück.

Diese Methode ist synchron und kann blockiert werden. Wenn die -Methode blockiert werden kann, sollte die [**CBaseInputPin::ReceiveCanBlock-Methode**](cbaseinputpin-receivecanblock.md) des Pins S \_ OK zurückgeben.

In der Basisklasse führt diese Methode die folgenden Schritte aus:

1.  Ruft die [**CBaseInputPin::CheckStreaming-Methode**](cbaseinputpin-checkstreaming.md) auf, um zu überprüfen, ob der Pin jetzt Beispiele verarbeiten kann. Wenn dies beispielsweise nicht dere ist, schlägt die -Methode fehl, wenn die Stecknadel beendet wird.
2.  Ruft die Beispieleigenschaften ab und überprüft, ob sich das Format geändert hat (siehe unten).
3.  Wenn sich das Format geändert hat, ruft die -Methode die [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf, um zu bestimmen, ob das neue Format akzeptabel ist.
4.  Wenn das neue Format nicht akzeptabel ist, ruft die -Methode die [**CBasePin::EndOfStream-Methode**](cbasepin-endofstream.md) auf, sendet ein EC \_ ERRORABORT-Ereignis und gibt einen Fehlercode zurück.
5.  Wenn keine Fehler aufgetreten sind, gibt die Methode S \_ OK zurück.

Testen Sie wie folgt, um eine Formatänderung zu erhalten:

-   Wenn das Beispiel die [**IMediaSample2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) unterstützt, überprüfen Sie den **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) Wenn das \_ AM SAMPLE \_ TYPECHANGED-Flag vorhanden ist, wurde das Format geändert.
-   Wenn das Beispiel **IMediaSample2** nicht unterstützt, rufen Sie andernfalls die [**IMediaSample::GetMediaType-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) auf. Wenn die Methode einen Wert ungleich **NULL** zurückgibt, wurde das Format geändert.

In der Basisklasse verarbeitet diese Methode das Beispiel nicht. Die abgeleitete Klasse muss diese Methode überschreiben, um die Verarbeitung durchzuführen. (Dies hängt vollständig vom Filter ab.) Die abgeleitete Klasse sollte die Basisklassenmethode aufrufen, um nach den zuvor beschriebenen Fehlern zu suchen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




