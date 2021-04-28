---
description: 'CSourceSeeking.SetPositions-Methode: Die SetPositions-Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die IMediaSeeking::SetPositions-Methode.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: CSourceSeeking.SetPositions-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085168"
---
# <a name="csourceseekingsetpositions-method"></a>CSourceSeeking.SetPositions-Methode

Die `SetPositions` -Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die [**IMediaSeeking::SetPositions-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCurrent* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Position angibt.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Bitweise Kombination von Flags. Siehe Hinweise.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Einheiten des aktuellen Zeitformats angibt.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Bitweise Kombination von Flags. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                  | Beschreibung                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültige Flags<br/>             |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Flags werden unterstützt:

-   AM \_ SEEKING \_ NoPositioning
-   AM \_ SEEKING \_ AbsolutePositioning
-   AM \_ SEEKING \_ RelativePositioning
-   AM \_ SEEKING \_ IncrementalPositioning ( nur *pStop)*

Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

Diese Methode aktualisiert die Werte der Membervariablen [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) und [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) und ruft dann die reinen virtuellen Methoden [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) und [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




