---
description: 'Mit der setsink-Methode wird ein externer Quality Manager festgelegt. Diese Methode implementiert die iqualitycontrol:: setsink-Methode.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Cbasepin. setsink-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356441"
---
# <a name="cbasepinsetsink-method"></a>Cbasepin. setsink-Methode

Mit der- `SetSink` Methode wird ein externer Quality Manager festgelegt. Diese Methode implementiert die [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piqc* 
</dt> <dd>

Ein Zeiger auf die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle von Quality Manager.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können Sie Qualitäts Steuerungs Meldungen an einen externen Quality Manager umleiten. Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




