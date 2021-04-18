---
description: Die performancealignwindow-Methode richtet die Fensterposition an DWORD-Begrenzungen aus, um eine maximale Leistung zu erzielen.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Cbasewindow. performancealignwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364449"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Cbasewindow. performancealignwindow-Methode

Die- `PerformanceAlignWindow` Methode richtet die Fensterposition an **DWORD** -Begrenzungen aus, um eine maximale Leistung zu erzielen.

## <a name="syntax"></a>Syntax


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode richtet den linken und oberen Rand des Fensters an DWORD-Begrenzungen aus, wodurch die Leistung verbessert werden kann. Wenn das Fenster über ein übergeordnetes Element verfügt, gibt die Methode S OK zurück, führt \_ jedoch die Ausrichtung aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




