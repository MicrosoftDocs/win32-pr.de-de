---
description: 'Die setmediatime-Methode legt die Medien Zeiten für dieses Beispiel fest. Diese Methode implementiert die imediasample:: setmediatime-Methode.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Cmediasample. setmediatime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357555"
---
# <a name="cmediasamplesetmediatime-method"></a>Cmediasample. setmediatime-Methode

Die- `SetMediaTime` Methode legt die Medien Zeiten für dieses Beispiel fest. Diese Methode implementiert die [**imediasample:: setmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Ein Zeiger auf die Start Zeit des Mediums oder **null**.

</dd> <dt>

*ausgesetzt* 
</dt> <dd>

Ein Zeiger auf die Endzeit des Mediums oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit für das Medien Ende muss höher sein als die Start Zeit des Mediums. Verwenden Sie **null** , um die Medien Zeiten für ungültig zu erklären.

Der *Pend* -Parameter gibt eine absolute Medien Zeit an, aber die [**cmediasample:: m \_ mediaend**](cmediasample-m-mediaend.md) -Member-Variable wird als Offset von *PStart* berechnet. Anders ausgedrückt: **m \_ mediaend**  =  \* *ptimeend* \* *ptimestart*.  

Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




