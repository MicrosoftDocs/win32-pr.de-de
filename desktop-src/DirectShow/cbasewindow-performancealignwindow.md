---
description: Die PerformanceAlignWindow-Methode richtet die Fensterposition an DWORD-Grenzen aus, um eine maximale Leistung zu erzielen.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: CBaseWindow.PerformanceAlignWindow-Methode (Winutil.h)
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
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016468"
---
# <a name="cbasewindowperformancealignwindow-method"></a>CBaseWindow.PerformanceAlignWindow-Methode

Die `PerformanceAlignWindow` -Methode richtet die Fensterposition an **DWORD-Grenzen** aus, um maximale Leistung zu erzielen.

## <a name="syntax"></a>Syntax


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode richtet den linken und oberen Rand des Fensters an DWORD-Grenzen aus, wodurch die Leistung verbessert werden kann. Wenn das Fenster über ein übergeordnetes Element verfügt, gibt die Methode S \_ OK zurück, führt jedoch die Ausrichtung aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




