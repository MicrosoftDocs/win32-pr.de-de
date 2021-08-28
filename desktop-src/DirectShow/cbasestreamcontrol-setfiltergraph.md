---
description: Die SetFilterGraph-Methode gibt die Ereignissenke für Streamsteuerungsereignisse an.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: CBaseStreamControl.SetFilterGraph-Methode (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502640"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>CBaseStreamControl.SetFilterGraph-Methode

Die `SetFilterGraph` -Methode gibt die Ereignissenke für Streamsteuerungsereignisse an.

## <a name="syntax"></a>Syntax


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSink* 
</dt> <dd>

Zeiger auf die [**IMediaEventSink Graph-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) des Filter-Managers oder **NULL,** wenn der Filter das Filterdiagramm verlässt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode innerhalb der [**IBaseFilter::JoinFilterGraph-Methode des Filters**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) auf. Die **CBaseStreamControl-Klasse** verwendet die **IMediaEventSink-Schnittstelle,** um [**EC STREAM CONTROL \_ \_ \_ STARTED-**](ec-stream-control-started.md) und [**EC STREAM CONTROL \_ \_ \_ STOPPED-Ereignisse zu**](ec-stream-control-stopped.md) senden.

Wenn Ihr Filter von **CBaseFilter** ableitung, rufen Sie zuerst die [**CBaseFilter::JoinFilterGraph-Methode**](cbasefilter-joinfiltergraph.md) auf, die die [**CBaseFilter::m \_ pSink-Membervariable**](cbasefilter-m-psink.md) legt. Übergeben Sie **dann m \_ pSink** an die `SetFilterGraph` -Methode. Beachten **Sie, \_ dass m pSink** **NULL ist,** wenn der Filter das Diagramm verlässt. Dies ist richtig.

## <a name="examples"></a>Beispiele


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




