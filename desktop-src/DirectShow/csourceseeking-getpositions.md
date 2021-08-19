---
description: Die GetPositions-Methode ruft die aktuelle Position und die Stoppposition ab. Diese Methode implementiert die IMediaSeeking::GetPositions-Methode.
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: CSourceSeeking.GetPositions-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073335"
---
# <a name="csourceseekinggetpositions-method"></a>CSourceSeeking.GetPositions-Methode

Die `GetPositions` -Methode ruft die aktuelle Position und die Stoppposition ab. Diese Methode implementiert die [**IMediaSeeking::GetPositions-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCurrent* 
</dt> <dd>

Zeiger auf eine Variable, die die Startposition empfängt.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppposition empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Für den *pCurrent-Parameter* gibt diese Methode den Wert der [**CSourceSeeking::m rtStart-Membervariablen \_**](csourceseeking-m-rtstart.md) zurück, die die letzte Suchzeit und nicht die aktuelle Streamingposition darstellt. Wenn eine Anwendung jedoch **IMediaSeeking::GetPositions** über den Filterdiagramm-Manager aufruft, stammen die Werte in der Regel aus einem Rendererfilter und nicht aus einem Quellfilter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




