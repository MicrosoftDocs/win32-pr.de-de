---
description: Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Cmediacontrol. gettypanfocount-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365629"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>Cmediacontrol. gettypanfocount-Methode

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

Ein Zeiger auf die Anzahl der vom Objekt bereitgestellten Schnittstellen vom Typ "Information". Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0 (null).

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

[**Cmediacontrol-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




