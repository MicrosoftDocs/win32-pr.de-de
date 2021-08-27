---
description: Die JoinFilterGraph-Methode sendet eine EC \_ WINDOW \_ DESTROYED-Ereignisbenachrichtigung, wenn ein Filter aus dem Filterdiagramm entfernt wird.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: CBaseVideoRenderer.JoinFilterGraph-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052210"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>CBaseVideoRenderer.JoinFilterGraph-Methode

Die -Methode sendet eine `JoinFilterGraph` EC WINDOW [**\_ \_ DESTROYED-Ereignisbenachrichtigung,**](ec-window-destroyed.md) wenn ein Filter aus dem Filterdiagramm entfernt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGraph* 
</dt> <dd>

Zeiger auf das Filterdiagramm, das verknüpft werden soll.

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Zeiger auf den Namen des filters, der hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion überschreibt die [**CBaseFilter::JoinFilterGraph-Memberfunktion.**](cbasefilter-joinfiltergraph.md) Wenn der Filter das Filterdiagramm verlässt *(pGraph* ist **NULL),** sendet er eine [**EC WINDOW \_ \_ DESTROYED-Ereignisbenachrichtigung,**](ec-window-destroyed.md) sodass der Ressourcen-Manager nicht als Fokusobjekt an den Renderer hält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




