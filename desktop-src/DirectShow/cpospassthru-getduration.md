---
description: 'CPosPassThru.GetDuration-Methode: Die GetDuration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetDuration-Methode.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: CPosPassThru.GetDuration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085578"
---
# <a name="cpospassthrugetduration-method"></a>CPosPassThru.GetDuration-Methode

Die `GetDuration` -Methode ruft die Dauer des Streams ab. Diese Methode implementiert die [**IMediaSeeking::GetDuration-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDuration* 
</dt> <dd>

Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeitformats empfängt.

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
</dt> </dl>

 

 




