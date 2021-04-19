---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Cbaseoutputpin. breakconnect-Methode (amfilter. h)
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
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372574"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Cbaseoutputpin. breakconnect-Methode

Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode. Er debugt die Zuweisung und gibt die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -und [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen frei.

Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen. Andernfalls können Sie Speicher Verluste verursachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




