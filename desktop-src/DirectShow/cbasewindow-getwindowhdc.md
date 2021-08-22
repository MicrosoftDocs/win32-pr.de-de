---
description: Die GetWindowHDC-Methode ruft ein Handle für den Gerätekontext des Fensters ab.
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: CBaseWindow.GetWindowHDC-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff0129e63e9a0c9808e36d73e37ff0e76d712b64c18e1e37ef88105797e2b495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074604"
---
# <a name="cbasewindowgetwindowhdc-method"></a>CBaseWindow.GetWindowHDC-Methode

Die `GetWindowHDC` -Methode ruft ein Handle für den Gerätekontext (DC) des Fensters ab.

## <a name="syntax"></a>Syntax


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für den DC zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




