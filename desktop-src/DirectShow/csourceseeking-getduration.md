---
description: 'CSourceSeeking.GetDuration-Methode: Die GetDuration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetDuration-Methode.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: CSourceSeeking.GetDuration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098768"
---
# <a name="csourceseekinggetduration-method"></a>CSourceSeeking.GetDuration-Methode

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

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Dauer wird von der [**CSourceSeeking::m \_ rtDuration-Membervariablen**](csourceseeking-m-rtduration.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




