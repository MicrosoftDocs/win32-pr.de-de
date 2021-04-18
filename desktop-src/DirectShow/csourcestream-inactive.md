---
description: 'Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist. Diese Methode überschreibt die cbasepin:: inaktive-Methode. Wenn der streamingingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Csourcestream. inaktive-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364717"
---
# <a name="csourcestreaminactive-method"></a>Csourcestream. inaktive-Methode

Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist. Diese Methode überschreibt die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode. Wenn der streamingingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




