---
description: Die inaktive Methode wird aufgerufen, wenn der Status in "beendet" versetzt wird.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Cbaserderderer. inaktive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364873"
---
# <a name="cbaserendererinactive-method"></a>Cbaserderderer. inaktive-Methode

Die- `Inactive` Methode wird aufgerufen, wenn der Zustand in "beendet" versetzt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: inaktiven**](crendererinputpin-inactive.md) -Methode auf. Der Filter Ruft die [**cbaserdenderer:: clearpdingsample**](cbaserenderer-clearpendingsample.md) -Methode auf, um das aktuelle Beispiel freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




