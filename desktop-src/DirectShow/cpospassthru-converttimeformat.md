---
description: 'CPosPassThru.ConvertTimeFormat-Methode: Die ConvertTimeFormat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die IMediaSeeking::ConvertTimeFormat-Methode.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: CPosPassThru.ConvertTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098958"
---
# <a name="cpospassthruconverttimeformat-method"></a>CPosPassThru.ConvertTimeFormat-Methode

Die `ConvertTimeFormat` -Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die [**IMediaSeeking::ConvertTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTarget* 
</dt> <dd>

Zeiger auf eine Variable, die die konvertierte Zeit empfängt.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Zeiger auf die GUID des Zeitformats des Zielformats. Bei **NULL** wird das aktuelle Format verwendet.

</dd> <dt>

*Quelle* 
</dt> <dd>

Der zu konvertierende Zeitwert.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Zeiger auf die Guid des Zeitformats des zu konvertierende Formats. Bei **NULL** wird das aktuelle Format verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeitformat-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




