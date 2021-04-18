---
description: 'Die ispreroll-Methode bestimmt, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die imediasample:: ispreroll-Methode.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Cmediasample. ispreroll-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358241"
---
# <a name="cmediasampleispreroll-method"></a>Cmediasample. ispreroll-Methode

Die- `IsPreroll` Methode bestimmt, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die [**imediasample:: ispreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn es sich bei dem Beispiel um ein vorab Beispiel handelt, \_ andernfalls "false".

## <a name="remarks"></a>Bemerkungen

Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




