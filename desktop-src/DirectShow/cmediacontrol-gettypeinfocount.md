---
description: 'CMediaControl.GetTypeInfoCount-Methode: Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.'
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: CMediaControl.GetTypeInfoCount-Methode (Ctlutil.h)
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
ms.openlocfilehash: 7b46838278414442d6c6fc64687fe21e02732e83
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095588"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>CMediaControl.GetTypeInfoCount-Methode

Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.

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

Zeiger auf die Anzahl der Typinformationsschnittstellen, die das -Objekt bereitstellt. Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ POINTER zurück, wenn *pctinfo* ungültig ist, andernfalls S \_ OK.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




