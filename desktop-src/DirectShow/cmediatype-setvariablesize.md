---
description: Die SetVariableSize-Methode gibt an, dass Beispiele keine feste Größe haben.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: CMediaType.SetVariableSize-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073964"
---
# <a name="cmediatypesetvariablesize-method"></a>CMediaType.SetVariableSize-Methode

Die `SetVariableSize` -Methode gibt an, dass Beispiele keine feste Größe haben.

## <a name="syntax"></a>Syntax


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt den **bFixedSizeSamples-Member** auf **FALSE fest.** Nachfolgende Aufrufe der [**CMediaType::GetSampleSize-Methode geben**](cmediatype-getsamplesize.md) 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




