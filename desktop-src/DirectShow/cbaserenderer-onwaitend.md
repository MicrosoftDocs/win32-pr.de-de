---
description: Die onwaitend-Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Cbaserenderer. onwaitend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358140"
---
# <a name="cbaserendereronwaitend-method"></a>Cbaserenderer. onwaitend-Methode

Die `OnWaitEnd` -Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet.

## <a name="syntax"></a>Syntax


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserderderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode ruft diese Methode auf, wenn Sie mit dem warten auf die Präsentationszeit eines Beispiels fertig ist. Diese Methode führt in der Basisklasse keine Aktionen aus, Sie kann jedoch von der abgeleiteten Klasse überschrieben werden.

Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**cbaserdenderer:: onwaitstart**](cbaserenderer-onwaitstart.md) -Methode überschreiben. Sie können diese Methoden verwenden, um die Leistung des Filters zu verfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




