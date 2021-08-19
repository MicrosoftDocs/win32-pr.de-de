---
description: Die SendNotifyWindow-Methode benachrichtigt den Upstreamfilter des Videofensterhandle.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: CBaseRenderer.SendNotifyWindow-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4956ad2b20040b0d22903d2ffaa2c7b460af9250fe057d106db545173d53a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157497"
---
# <a name="cbaserenderersendnotifywindow-method"></a>CBaseRenderer.SendNotifyWindow-Methode

Die `SendNotifyWindow` -Methode benachrichtigt den Upstreamfilter des Videofensterhandle.

## <a name="syntax"></a>Syntax


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Ausgabepins des Upstreamfilters.

</dd> <dt>

*Hwnd* 
</dt> <dd>

Handle für das Videofenster oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Ausgabepin des Upstreamfilters die [**IMediaEventSink-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) unterstützt, sendet diese Methode ihm den [**EC NOTIFY \_ \_ WINDOW-Ereigniscode**](ec-notify-window.md) zusammen mit dem Fensterhandle.

Videorenderer können ihre [**CBaseRenderer::CompleteConnect-Methoden**](cbaserenderer-completeconnect.md) überschreiben, um diese Methode aufzurufen. Sie bietet einen Mechanismus zum Informieren des Upstreamfilters des Fensterhandle. Wenn Sie dies tun, überschreiben Sie auch die [**CBaseRenderer::BreakConnect-Methode,**](cbaserenderer-breakconnect.md) und rufen Sie `SendNotifyWindow` mit einem **NULL-Handle** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




