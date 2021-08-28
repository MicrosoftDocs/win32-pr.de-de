---
description: Die GetResult-Methode ruft die resultierende Argumentliste ab, sofern vorhanden.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: CDeferredCommand.GetResult-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2176d6787bd520517cccbf484bdf6642921d499aaeb97c2917d64fa148323b66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076420"
---
# <a name="cdeferredcommandgetresult-method"></a>CDeferredCommand.GetResult-Methode

Die `GetResult` -Methode ruft die resultierende Argumentliste ab, sofern vorhanden.

## <a name="syntax"></a>Syntax


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine **VARIANT** zurück, die die Argumentliste der Methode enthält, sofern vorhanden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




