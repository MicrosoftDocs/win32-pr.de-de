---
description: 'Die setsyncpoint-Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die imediasample:: setsyncpoint-Methode.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Cmediasample. setsyncpoint-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352850"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Cmediasample. setsyncpoint-Methode

Die- `SetSyncPoint` Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die [**imediasample:: setsyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bissyncpoint* 
</dt> <dd>

Boolescher Wert, der angibt, ob es sich um einen Synchronisierungs Punkt handelt. **True** gibt an, dass dies ein Synchronisierungs Punkt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die Synchronisierungs Punkt Eigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




