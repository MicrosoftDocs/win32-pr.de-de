---
description: Die initializeoutputsample-Methode ruft eine neue Ausgabe Stichprobe ab und initialisiert sie.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Initializeoutputsample-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359707"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.Initializeoutputsample-Methode

Die `InitializeOutputSample` -Methode ruft eine neue Ausgabe Stichprobe ab und initialisiert sie.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle der Eingabe Stichprobe.

</dd> <dt>

*ppoutsample* 
</dt> <dd>

Empfängt einen Zeiger auf die **imediasample** -Schnittstelle des Ausgabe Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode aufgerufen, um das Ausgabe Beispiel vorzubereiten. Im Allgemeinen müssen Sie diese Methode nicht in der abgeleiteten Klasse aufzurufen, es sei denn, Sie überschreiben die **Receive** -Methode.

Diese Methode ruft ein neues Beispiel aus der Zuweisung der Ausgabe-PIN ab. Anschließend werden die Beispiel Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert. Die Beispiel Eigenschaften werden in der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




