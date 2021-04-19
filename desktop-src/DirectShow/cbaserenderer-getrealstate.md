---
description: Die getrealstate-Methode ruft den Filter Zustand ab.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Cbaserderderer. getrealstate-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356375"
---
# <a name="cbaserenderergetrealstate-method"></a>Cbaserderderer. getrealstate-Methode

Die- `GetRealState` Methode ruft den Filter Zustand ab.

## <a name="syntax"></a>Syntax


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des [**cbasefilter:: m- \_ Zustands**](cbasefilter-m-state.md)zurück. Der Wert ist ein Member des Enumerationstyps [**Filter \_ Status**](/windows/win32/api/strmif/ne-strmif-filter_state) .

## <a name="remarks"></a>Bemerkungen

Diese Methode stellt eine einfachere Alternative zur [**cbaserdenderer:: GetState**](cbaserenderer-getstate.md) -Methode zur internen Verwendung bereit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




