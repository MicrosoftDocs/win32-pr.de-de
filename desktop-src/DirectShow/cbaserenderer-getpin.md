---
description: Die getpin-Methode ruft eine PIN ab.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Cbaserderderer. getpin-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358268"
---
# <a name="cbaserenderergetpin-method"></a>Cbaserderderer. getpin-Methode

Die- `GetPin` Methode ruft eine PIN ab.

## <a name="syntax"></a>Syntax


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Nummer der angegebenen PIN. Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**cbaserenderer:: m \_ pinputpin**](cbaserenderer-m-pinputpin.md) -Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode, die rein virtuell in der **cbasefilter** -Klasse ist. Der Filter unterstützt genau eine PIN (die Eingabe-PIN). Beim ersten Aufruf dieser Methode wird die PIN als neues [**crendererinputpin**](crendererinputpin.md) -Objekt erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




