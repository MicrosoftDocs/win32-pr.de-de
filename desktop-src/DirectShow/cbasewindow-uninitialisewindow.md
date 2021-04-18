---
description: Die uninitialierwindow-Methode gibt die Fenster Ressourcen frei.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Cbasewindow. uninitialierwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361056"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Cbasewindow. uninitialicwindow-Methode

Die `UninitialiseWindow` -Methode gibt die Fenster Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt Ressourcen frei, die von der [**cbasewindow:: initialicwindow**](cbasewindow-initialisewindow.md) -Methode abgerufen wurden. Die [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) -Methode ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




