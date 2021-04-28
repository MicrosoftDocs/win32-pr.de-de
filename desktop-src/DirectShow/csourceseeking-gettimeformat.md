---
description: 'CSourceSeeking.GetTimeFormat-Methode: Die GetTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die IMediaSeeking::GetTimeFormat-Methode.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: CSourceSeeking.GetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085218"
---
# <a name="csourceseekinggettimeformat-method"></a>CSourceSeeking.GetTimeFormat-Methode

Die `GetTimeFormat` -Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die [**IMediaSeeking::GetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt. Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

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

 

 




