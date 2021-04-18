---
description: 'Die isformatsupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die imediaseeking:: isformatsupported-Methode.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Cpospassthru. isformatsupported-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364474"
---
# <a name="cpospassthruisformatsupported-method"></a>Cpospassthru. isformatsupported-Methode

Die- `IsFormatSupported` Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die [**imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsFormatSupported(
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

 

 




