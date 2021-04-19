---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Ctransformoutputpin. breakconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316806b89adf6493f32125da488990151f0916b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352976"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Ctransformoutputpin. breakconnect-Methode

Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin:: breakconnect**](cbaseoutputpin-breakconnect.md) -Methode. Er ruft die [**ctransformfilter:: breakconnect**](ctransformfilter-breakconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt. Die abgeleitete Klasse kann die **ctransformfilter:: breakconnect** -Methode überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




