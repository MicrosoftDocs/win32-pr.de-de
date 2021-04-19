---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Ctransforminputpin. breakconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359793"
---
# <a name="ctransforminputpinbreakconnect-method"></a>Ctransforminputpin. breakconnect-Methode

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

Diese Methode überschreibt die [**cbasinput PIN:: breakconnect**](cbaseinputpin-breakconnect.md) -Methode. Er ruft die [**ctransformfilter:: breakconnect**](ctransformfilter-breakconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt. Die abgeleitete Klasse kann die **ctransformfilter:: breakconnect** -Methode überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




