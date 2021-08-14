---
description: Die UninitialiseWindow-Methode gibt die Ressourcen des Fensters frei.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: CBaseWindow.UninitialiseWindow-Methode (Winutil.h)
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
ms.openlocfilehash: c275e4d683bcc698c8f04c5a85017b081b6aad17f93c91d66e0a75f2da88692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657492"
---
# <a name="cbasewindowuninitialisewindow-method"></a>CBaseWindow.UninitialiseWindow-Methode

Die `UninitialiseWindow` -Methode gibt die Ressourcen des Fensters frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode gibt Ressourcen frei, die von der [**CBaseWindow::InitialiseWindow-Methode**](cbasewindow-initialisewindow.md) erworben wurden. Die [**CBaseWindow::D oneWithWindow-Methode**](cbasewindow-donewithwindow.md) ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




