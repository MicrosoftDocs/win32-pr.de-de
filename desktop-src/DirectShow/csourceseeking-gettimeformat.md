---
description: 'Die getTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die imediaseeking:: getTimeFormat-Methode.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Csourceseeking. getTimeFormat-Methode (ctlutil. h)
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
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372121"
---
# <a name="csourceseekinggettimeformat-method"></a>Csourceseeking. getTimeFormat-Methode

Die- `GetTimeFormat` Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die [**imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt. Siehe [**Zeit Format-GUIDs**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




