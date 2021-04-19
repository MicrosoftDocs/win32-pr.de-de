---
description: 'Die getpositions-Methode ruft die aktuelle Position und die Position des Stopps ab. Diese Methode implementiert die imediaseeking:: getpositions-Methode.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Csourceseeking. getpositions-Methode (ctlutil. h)
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
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366752"
---
# <a name="csourceseekinggetpositions-method"></a>Csourceseeking. getpositions-Methode

Die `GetPositions` -Methode ruft die aktuelle Position und die Position des Stopps ab. Diese Methode implementiert die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startposition empfängt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Position des Stopps empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Für den *pcurrent* -Parameter gibt diese Methode den Wert der [**csourceseeking:: m \_ rtstart**](csourceseeking-m-rtstart.md) -Member-Variable zurück, die die letzte Suchzeit und nicht die aktuelle streamingposition darstellt. Wenn eine Anwendung jedoch **imediaseeking:: getpositions** über den Filter Graph-Manager aufruft, werden die Werte in der Regel von einem rendererfilter und keinem Quell Filter abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




