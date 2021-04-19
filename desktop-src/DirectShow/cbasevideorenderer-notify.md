---
description: Die Benachrichtigungs Methode erhält eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Cbasevideorenderer. Notify-Methode (renbase. h)
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
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356402"
---
# <a name="cbasevideorenderernotify-method"></a>Cbasevideorenderer. Notify-Methode

Die- `Notify` Methode empfängt eine Benachrichtigung, dass eine Qualitätsänderung angefordert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pself* \[ in\]
</dt> <dd>

Zeiger auf den Filter, der die Qualitäts Benachrichtigung sendet.

</dd> <dt>

*q* \[ in\]
</dt> <dd>

Qualitätsbenachrichtigungs-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode für den Videorenderer. Dies wird in der Regel vom Filter Graph-Manager aufgerufen, wenn die Qualität gekürzt werden muss. Dies kann vorkommen, wenn die Qualität der Audiowiedergabe auf den Punkt angehoben wurde, an dem die Qualität der Videowiedergabe gesenkt werden muss.

`Notify` Legt den **m \_ trthrottle** -Datenmember auf einen Verzögerungswert fest, der durch [**throttlewait**](cbasevideorenderer-throttlewait.md)zwischen Frames eingefügt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




