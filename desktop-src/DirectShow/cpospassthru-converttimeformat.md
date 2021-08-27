---
description: 'CPosPassThru.ConvertTimeFormat-Methode: Die ConvertTimeFormat-Methode konvertiert ein Zeitformat in ein anderes. Diese Methode implementiert die IMediaSeeking::ConvertTimeFormat-Methode.'
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
ms.openlocfilehash: 2382d36899bf7e3ac85e217502a878497274604ced4b77cf7acbc1465586c487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954119"
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

Zeiger auf die Zeitformat-GUID des Zielformats. Bei **NULL** wird das aktuelle Format verwendet.

</dd> <dt>

*Quelle* 
</dt> <dd>

Der zu konvertierte Zeitwert.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Zeiger auf die Zeitformat-GUID des zu konvertierenden Formats. Bei **NULL** wird das aktuelle Format verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeitformat-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




