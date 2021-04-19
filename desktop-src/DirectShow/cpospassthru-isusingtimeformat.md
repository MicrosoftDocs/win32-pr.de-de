---
description: 'Die isusingtimeformat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist. Diese Methode implementiert die imediaseeking:: isusingtimeformat-Methode.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Cpospassthru. isusingtimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359817"
---
# <a name="cpospassthruisusingtimeformat-method"></a>Cpospassthru. isusingtimeformat-Methode

Die- `IsUsingTimeFormat` Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist. Diese Methode implementiert die [**imediaseeking:: isusingtimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Zeiger auf eine Zeitformat-GUID.

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

 

 




