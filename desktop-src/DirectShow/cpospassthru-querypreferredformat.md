---
description: 'Die querypreferredformat-Methode ruft das bevorzugte Zeitformat für den Stream ab. Diese Methode implementiert die imediaseeking:: querypreferredformat-Methode.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Cpospassthru. querypreferredformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372058"
---
# <a name="cpospassthruquerypreferredformat-method"></a>Cpospassthru. querypreferredformat-Methode

Die- `QueryPreferredFormat` Methode ruft das bevorzugte Zeitformat für den Stream ab. Diese Methode implementiert die [**imediaseeking:: querypreferredformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeit Format-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




