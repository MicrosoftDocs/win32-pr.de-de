---
description: 'CPosPassThru.IsFormatSupported-Methode: Die IsFormatSupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die IMediaSeeking::IsFormatSupported-Methode.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: CPosPassThru.IsFormatSupported-Methode (Ctlutil.h)
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
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095248"
---
# <a name="cpospassthruisformatsupported-method"></a>CPosPassThru.IsFormatSupported-Methode

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

Zeiger auf eine Zeitformat-GUID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeitformat-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




