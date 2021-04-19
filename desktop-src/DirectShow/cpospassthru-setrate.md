---
description: 'Die setRate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaseeking:: Server trate-Methode.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Cpospassthru. ctrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357692"
---
# <a name="cpospassthrusetrate-method"></a>Cpospassthru. ctrate-Methode

Die- `SetRate` Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die [**imediaseeking:: Server trate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*drate* 
</dt> <dd>

Wiedergabe Rate. Darf nicht NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ invalidArg zurück, wenn *drate* 0 (null) ist. Andernfalls wird der **HRESULT** -Wert aus der verbundenen Pin zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




