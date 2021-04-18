---
description: Die checkready-Methode fragt ab, ob ein Zustandsübergang abgeschlossen ist.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Cbaserderderer. checkready-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371196"
---
# <a name="cbaserenderercheckready-method"></a>Cbaserderderer. checkready-Methode

Die- `CheckReady` Methode fragt ab, ob ein Zustandsübergang beendet ist.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn der Zustandsübergang beendet ist, oder " **false** ", wenn der Filter weiterhin in einen neuen Zustand übergeht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**Cbaserderderer:: notready**](cbaserenderer-notready.md)
</dt> <dt>

[**Cbasererderer:: Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




