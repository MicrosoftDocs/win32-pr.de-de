---
description: Die setfiltergraph-Methode gibt die Ereignis Senke für streamsteuerungsereignisse an.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Cbasestreamcontrol. setfiltergraph-Methode ("strinmctl. h")
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
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363208"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Cbasestreamcontrol. setfiltergraph-Methode

Die- `SetFilterGraph` Methode gibt die Ereignis Senke für streamsteuerungsereignisse an.

## <a name="syntax"></a>Syntax


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psink* 
</dt> <dd>

Ein Zeiger auf die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle des Filter Diagramm-Managers oder **null** , wenn der Filter das Filter Diagramm verlässt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird innerhalb der [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode des Filters aufgerufen. Die **cbasestreamcontrol** -Klasse verwendet die **imediaeventsink** -Schnittstelle, um das [**gestartete EC- \_ Stream- \_ Steuer \_**](ec-stream-control-started.md) Element zu senden, und Ereignisse, die von der [**\_ \_ \_**](ec-stream-control-stopped.md)

Wenn der Filter von **cbasefilter** abgeleitet ist, müssen Sie zuerst die [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Methode aufzurufen, mit der die [**cbasefilter:: m \_ psink**](cbasefilter-m-psink.md) -Element Variable festgelegt wird. Übergeben Sie dann **m \_ psink** an die- `SetFilterGraph` Methode. Beachten Sie, dass **m \_ psink** **null** ist, wenn der Filter das Diagramm verlässt, was korrekt ist.

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
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




