---
description: 'CPosPassThru.GetTimeFormat-Methode: Die GetTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die IMediaSeeking::GetTimeFormat-Methode.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: CPosPassThru.GetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903d1c6163d4cad5c5b9ca22213b02542bb3da49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085588"
---
# <a name="cpospassthrugettimeformat-method"></a>CPosPassThru.GetTimeFormat-Methode

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

Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.

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

 

 




