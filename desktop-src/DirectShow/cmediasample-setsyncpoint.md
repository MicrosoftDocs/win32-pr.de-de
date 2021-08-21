---
description: Die SetSyncPoint-Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungspunkt ist. Diese Methode implementiert die IMediaSample::SetSyncPoint-Methode.
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: CMediaSample.SetSyncPoint-Methode (Amfilter.h)
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
ms.openlocfilehash: 0be51ed18e25bcbd12e33f9167493d73f0c140480f4ec0042fb0c43928720d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156522"
---
# <a name="cmediasamplesetsyncpoint-method"></a>CMediaSample.SetSyncPoint-Methode

Die `SetSyncPoint` -Methode gibt an, ob der Anfang dieses Beispiels ein Synchronisierungspunkt ist. Diese Methode implementiert die [**IMediaSample::SetSyncPoint-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

Boolescher Wert, der angibt, ob dies ein Synchronisierungspunkt ist. True gibt an, dass dies ein Synchronisierungspunkt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode aktualisiert die [**Membervariable CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) die die Synchronisierungspunkteigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




