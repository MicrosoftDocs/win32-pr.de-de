---
description: Die QueryPreferredFormat-Methode ruft das bevorzugte Zeitformat für den Stream ab. Diese Methode implementiert die IMediaSeeking::QueryPreferredFormat-Methode.
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: CPosPassThru.QueryPreferredFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6744516f52a22bf322670388295c55f15f19d19c1b3e5896bba1a66e0668a30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757040"
---
# <a name="cpospassthruquerypreferredformat-method"></a>CPosPassThru.QueryPreferredFormat-Methode

Die `QueryPreferredFormat` -Methode ruft das bevorzugte Zeitformat für den Stream ab. Diese Methode implementiert die [**IMediaSeeking::QueryPreferredFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.

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

 

 




