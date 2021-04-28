---
description: 'CSourceSeeking.ConvertTimeFormat-Methode: Die ConvertTimeFormat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die IMediaSeeking::ConvertTimeFormat-Methode.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: CSourceSeeking.ConvertTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085248"
---
# <a name="csourceseekingconverttimeformat-method"></a>CSourceSeeking.ConvertTimeFormat-Methode

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

Zeiger auf die GUID des Zielformats. Bei **NULL** wird das aktuelle Format verwendet. Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)

</dd> <dt>

*Quelle* 
</dt> <dd>

Der zu konvertierende Zeitwert.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Zeiger auf die GUID des Zeitformats des zu konvertierende Formats. Bei **NULL** wird das aktuelle Format verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                  | Beschreibung                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument<br/>          |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das einzige von der Basisklasse unterstützte Zeitformat ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden). Diese Methode gibt E INVALIDARG zurück, außer in dem trivialen Fall, in dem \_ *sowohl pTargetFormat* als auch *pSourceFormat* TIME \_ FORMAT MEDIA TIME \_ \_ angeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




