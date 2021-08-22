---
description: Die IsUsingTimeFormat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist. Diese Methode implementiert die IMediaSeeking::IsUsingTimeFormat-Methode.
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: CPosPassThru.IsUsingTimeFormat-Methode (Ctlutil.h)
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
ms.openlocfilehash: 64c240a0b1c269dde57e07e50bcbdbbd4d5d7e03d24a4e6d263662947f3d65de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954009"
---
# <a name="cpospassthruisusingtimeformat-method"></a>CPosPassThru.IsUsingTimeFormat-Methode

Die `IsUsingTimeFormat` -Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist. Diese Methode implementiert die [**IMediaSeeking::IsUsingTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine Zeitformat-GUID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeitformat-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




