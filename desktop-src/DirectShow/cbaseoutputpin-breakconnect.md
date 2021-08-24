---
description: 'CBaseOutputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin aus einer Verbindung frei.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: CBaseOutputPin.BreakConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae03edb843a2b9c6f1cbc98a46c2464de0e76e2eecf5d77bc309efa2dd60fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793219"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>CBaseOutputPin.BreakConnect-Methode

Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::BreakConnect-Methode.**](cbasepin-breakconnect.md) Er decommitiert die Zuweisung und gibt die [**Schnittstellen IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) und [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) frei.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf. Andernfalls können Speicherverlusten verursacht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




