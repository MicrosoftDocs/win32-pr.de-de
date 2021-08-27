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
ms.openlocfilehash: 92349ab37fb677b561f342e99882c27208287310b544880e397f4f5df6cb0c38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083920"
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



 

## <a name="remarks"></a>Hinweise

Das einzige zeitformat, das von der Basisklasse unterstützt wird, ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




