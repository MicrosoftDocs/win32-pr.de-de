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
ms.openlocfilehash: a751c7ed9d10547d34ec491f2e90e5ca6f1ab1f19bc1221c04b15da427da4570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832520"
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

Zeiger auf die Anzahl der Typinformationsschnittstellen, die das -Objekt bereitstellt. Wenn das -Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ POINTER zurück, wenn *pctinfo* ungültig ist, andernfalls S \_ OK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




