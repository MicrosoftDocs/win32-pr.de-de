---
description: 'Die Methode "beenden" beendet das-Objekt. Diese Methode implementiert die imediafilter:: stopmethode.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Cbasemediafilter. stoppt-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359244"
---
# <a name="cbasemediafilterstop-method"></a>Cbasemediafilter. stoppt-Methode

Die- `Stop` Methode beendet das-Objekt. Diese Methode implementiert die [**imediafilter:: stopmethode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse legt diese Methode die " [**cbasemediafilter:: m \_ State**](cbasemediafilter-m-state.md) Member"-Variable auf "beendet" fest, bewirkt \_ aber nichts anderes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




