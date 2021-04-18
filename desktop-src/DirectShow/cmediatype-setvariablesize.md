---
description: Die setvariablesize-Methode gibt an, dass die Beispiele keine festgelegte Größe aufweisen.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Cmediatype. setvariablesize-Methode (mtype. h)
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
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364470"
---
# <a name="cmediatypesetvariablesize-method"></a>Cmediatype. setvariablesize-Methode

Die- `SetVariableSize` Methode gibt an, dass die-Beispiele keine festgelegte Größe aufweisen.

## <a name="syntax"></a>Syntax


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt das **bfixedsizesamples** -Element auf " **false**" fest. Nachfolgende Aufrufe der [**cmediatype:: getSampleSize**](cmediatype-getsamplesize.md) -Methode geben 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




