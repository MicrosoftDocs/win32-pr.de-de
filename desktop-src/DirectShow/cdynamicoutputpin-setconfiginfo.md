---
description: Die SetConfigInfo-Methode gibt den IGraphConfig-Zeiger und das Stop-Ereignis an.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: CDynamicOutputPin.SetConfigInfo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23b492eaf4b5f712a51132eefcceac12a772b17b8285d8c6edb1a6cec268b1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074234"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>CDynamicOutputPin.SetConfigInfo-Methode

Die `SetConfigInfo` -Methode gibt den [**IGraphConfig-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) und das Beendigungsereignis an.

## <a name="syntax"></a>Syntax


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

Zeiger auf die [**IGraphConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) oder **NULL.**

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Behandeln Sie ein Ereignis, das signalisiert wird, wenn der Filter beendet wird, oder **NULL**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Filter muss diese Methode aufrufen, wenn er dem Filterdiagramm beitritt. Der Filtergraph-Manager unterstützt **IGraphConfig.** Erstellen Sie für den *Parameter hStopEvent* ein Ereignis für die manuelle Zurücksetzung. Wenn der Filter das Filterdiagramm verlässt, rufen Sie diese Methode für beide Parameter erneut mit **NULL** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




