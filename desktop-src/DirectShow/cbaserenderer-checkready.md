---
description: Die CheckReady-Methode fragt ab, ob ein Zustandsübergang abgeschlossen ist.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: CBaseRenderer.CheckReady-Methode (Renbase.h)
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
ms.openlocfilehash: 9a1fac55eba92141ac8174b30ed2dcbc4685ba250b7bb21236432bb998b3b5e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043950"
---
# <a name="cbaserenderercheckready-method"></a>CBaseRenderer.CheckReady-Methode

Die `CheckReady` -Methode fragt ab, ob ein Zustandsübergang abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Zustandsübergang abgeschlossen ist, oder **FALSE,** wenn der Filter noch in einen neuen Zustand über geht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer::Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




