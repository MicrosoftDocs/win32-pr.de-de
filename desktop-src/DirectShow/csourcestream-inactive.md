---
description: Die inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist. Diese Methode überschreibt die CBasePin::Inactive-Methode. Wenn der Streamingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: CSourceStream.Inactive-Methode (Source.h)
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
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687370"
---
# <a name="csourcestreaminactive-method"></a>CSourceStream.Inactive-Methode

Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist. Diese Methode überschreibt die [**CBasePin::Inactive-Methode.**](cbasepin-inactive.md) Wenn der Streamingthread aktiv ist, beendet diese Methode ihn und wartet, bis der Thread beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




