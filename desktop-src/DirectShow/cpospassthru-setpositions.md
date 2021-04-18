---
description: 'Die setpositions-Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die imediaseeking:: setpositions-Methode.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Cpospassthru. setpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361050"
---
# <a name="cpospassthrusetpositions-method"></a>Cpospassthru. setpositions-Methode

Die `SetPositions` -Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats angibt.

</dd> <dt>

*dwcurrentflags* 
</dt> <dd>

Bitweise Kombination von-Flags. Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats angibt.

</dd> <dt>

*dwstopflags* 
</dt> <dd>

Bitweise Kombination von-Flags. Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




