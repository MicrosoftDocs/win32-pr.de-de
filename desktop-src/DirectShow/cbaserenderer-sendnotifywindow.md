---
description: Die sendnotifywindow-Methode benachrichtigt den upstreamfilter über das Videofenster handle.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Cbaserenderer. sendnotifywindow-Methode (renbase. h)
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
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369625"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Cbaserenderer. sendnotifywindow-Methode

Die- `SendNotifyWindow` Methode benachrichtigt den upstreamfilter über das Videofenster handle.

## <a name="syntax"></a>Syntax


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabepin des Upstream-Filters.

</dd> <dt>

*HWND* 
</dt> <dd>

Handle für das Videofenster oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Ausgabe-PIN des Upstream-Filters die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle unterstützt, sendet diese Methode den Ereignis Code des [**EC- \_ Benachrichtigungs \_ Fensters**](ec-notify-window.md) zusammen mit dem Fenster handle.

Videorenderer können Ihre [**cbaserdenderer:: completeconnect**](cbaserenderer-completeconnect.md) -Methoden überschreiben, um diese Methode aufzurufen. Es stellt einen Mechanismus bereit, mit dem der upstreamfilter des Fenster Handles informiert werden kann. Wenn Sie dies tun, überschreiben Sie auch die [**cbaserdenderer:: breakconnect**](cbaserenderer-breakconnect.md) -Methode, und wenden Sie `SendNotifyWindow` mit einem **null** -Handle an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




