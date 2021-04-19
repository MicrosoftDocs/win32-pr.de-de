---
description: Die onwaitstart-Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Cbaserderderer. onwaitstart-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362153"
---
# <a name="cbaserendereronwaitstart-method"></a>Cbaserderderer. onwaitstart-Methode

Die `OnWaitStart` -Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.

## <a name="syntax"></a>Syntax


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserderderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode ruft diese Methode auf, wenn Sie beginnt, auf die Präsentationszeit eines Beispiels zu warten. Diese Methode führt in der Basisklasse keine Aktionen aus, Sie kann jedoch von der abgeleiteten Klasse überschrieben werden.

Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**cbaserenderer:: onwaitend**](cbaserenderer-onwaitend.md) -Methode überschreiben. Sie können diese Methoden verwenden, um die Leistung des Filters zu verfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




