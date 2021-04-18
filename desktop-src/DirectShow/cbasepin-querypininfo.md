---
description: 'Die querypininfo-Methode ruft Informationen über die PIN ab. Diese Methode implementiert die IPin:: querypininfo-Methode.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Cbasepin. querypininfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368540"
---
# <a name="cbasepinquerypininfo-method"></a>Cbasepin. querypininfo-Methode

Die- `QueryPinInfo` Methode ruft Informationen über die PIN ab. Diese Methode implementiert die [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* 
</dt> <dd>

Zeiger auf eine [**Pin- \_ Info**](/windows/win32/api/strmif/ns-strmif-pin_info) -Struktur, die die PIN-Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode verwendet die [**cbasepin:: m \_ PName**](cbasepin-m-pname.md) -Member-Variable für den **achname** -Member der PIN \_ Info-Struktur.

Wenn die-Methode zurückgibt, hat der **pFilter** -Member der PIN \_ -Informationsstruktur einen ausstehenden Verweis Zähler, wenn er nicht **null** ist. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




