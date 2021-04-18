---
description: Die aktive Methode wird aufgerufen, wenn der Zustand zum Anhalten oder ausführen gewechselt wird.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Cbaserderderer. Active-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371605"
---
# <a name="cbaserendereractive-method"></a>Cbaserderderer. Active-Methode

Die- `Active` Methode wird aufgerufen, wenn der Zustand zum Anhalten oder ausführen gewechselt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: Active**](crendererinputpin-active.md) -Methode auf. Diese Methode führt in der Basisklasse keine Aktion aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




