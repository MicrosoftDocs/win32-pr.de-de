---
description: 'CSourceSeeking.IsFormatSupported-Methode: Die IsFormatSupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die IMediaSeeking::IsFormatSupported-Methode.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: CSourceSeeking.IsFormatSupported-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098748"
---
# <a name="csourceseekingisformatsupported-method"></a>CSourceSeeking.IsFormatSupported-Methode

Die `IsFormatSupported` -Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die [**IMediaSeeking::IsFormatSupported-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)

## <a name="syntax"></a>Syntax


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine GUID im Zeitformat. Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Das Format wird nicht unterstützt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Das Format wird unterstützt.<br/>     |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerargument.**<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Das einzige zeitformat, das von der Basisklasse unterstützt wird, ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




