---
description: Die nächste Methode ruft die nächste Position in der Liste ab.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Cbaselist. Next-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367049"
---
# <a name="cbaselistnext-method"></a>Cbaselist. Next-Methode

Die- `Next` Methode ruft die nächste Position in der Liste ab.

## <a name="syntax"></a>Syntax


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator zurück, der der von *POS* angegebenen Position folgt.

## <a name="remarks"></a>Bemerkungen

Wenn *POS* die letzte Position in der Liste ist, gibt die Methode **null** zurück. Wenn *POS* **null** ist, gibt die Methode die erste Position in der Liste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




