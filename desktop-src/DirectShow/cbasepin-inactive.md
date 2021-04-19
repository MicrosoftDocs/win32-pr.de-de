---
description: Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Cbasepin. ininaktive Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370180"
---
# <a name="cbasepininactive-method"></a>Cbasepin. inaktive-Methode

Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter angehalten wird, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode auf allen verbundenen Pins des Filters auf.

Diese Methode führt in der Basisklasse keine Aktion aus. Abgeleitete Klassen sollten diese Methode überschreiben, um alle Ressourcen freizugeben, die von der [**cbasepin:: Active**](cbasepin-active.md) -Methode abgerufen werden. beispielsweise, um die Zuweisungen der PIN zu decoden.

Der interne Zustand des Filter Graph-Managers wird erst aktualisiert, nachdem diese Methode zurückgegeben wurde. Testen Sie daher nicht den Status dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




