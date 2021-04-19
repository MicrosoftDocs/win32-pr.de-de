---
description: Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Cmediaevent. gettypeingefocount-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369624"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Cmediaevent. gettypeingefocount-Methode

Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pctinfo* 
</dt> <dd>

Zeiger auf die Anzahl von Typ-Informations Schnittstellen, die das Objekt bereitstellt. Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen E- \_ Zeiger zurück, wenn *pctinfo* ungültig ist; andernfalls gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaevent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




