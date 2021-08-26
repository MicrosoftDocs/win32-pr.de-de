---
description: Die Notify-Methode empfängt eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: CBaseVideoRenderer.Notify-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052190"
---
# <a name="cbasevideorenderernotify-method"></a>CBaseVideoRenderer.Notify-Methode

Die `Notify` -Methode empfängt eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSelf* \[ In\]
</dt> <dd>

Zeiger auf den Filter, der die Qualitätsbenachrichtigung sendet.

</dd> <dt>

*q* \[ in\]
</dt> <dd>

Struktur von Qualitätsbenachrichtigungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IQualityControl::Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) für den Videorenderer. Dies wird in der Regel vom Filterdiagramm-Manager aufgerufen, wenn die Qualität zurückgesetzt werden muss. Dies kann auftreten, wenn die Qualität der Audiowiedergabe auf den Punkt erhöht wurde, dass die Qualität der Videowiedergabe verringert werden muss.

`Notify` legt den **m \_ trThrottle-Daten** member auf einen Verzögerungswert fest, der von [**ThrottleWait**](cbasevideorenderer-throttlewait.md)zwischen Frames eingefügt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




