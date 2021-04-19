---
description: 'Die setRate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaseeking:: Server trate-Methode.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Csourceseeking. ctrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354190"
---
# <a name="csourceseekingsetrate-method"></a>Csourceseeking. ctrate-Methode

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

Wiedergabe Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode aktualisiert den Wert der [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) -Element Variablen und ruft dann die rein virtuelle Methode [**csourceseeking:: changerate**](csourceseeking-changerate.md)auf. Der *drate* -Parameter wird von der-Methode nicht überprüft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




