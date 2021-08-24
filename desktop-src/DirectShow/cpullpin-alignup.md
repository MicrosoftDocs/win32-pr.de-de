---
description: Die AlignUp-Methode rundet einen Wert auf eine angegebene Ausrichtungsgrenze. Hinweis Entfernt in Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: CPullPin.AlignUp-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34c45fe4a34e21647cd976adbf29dfe6723e4216d58166e7d1599d4c8d64d47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687760"
---
# <a name="cpullpinalignup-method"></a>CPullPin.AlignUp-Methode

Die **AlignUp-Methode** rundet einen Wert auf eine angegebene Ausrichtungsgrenze.

> [!Note]  
> In Windows 7 entfernt.

 

## <a name="syntax"></a>Syntax


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ll* 
</dt> <dd>

Gibt die Zahl an, die ausgerichtet werden soll.

</dd> <dt>

*lAlign* 
</dt> <dd>

Gibt die Ausrichtungsgrenze an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das ausgerichtete Ergebnis zurück.

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Diese Methode kann einen numerischen Überlauf verursachen, wenn *ll* + (*lAlign* - 1) überläuft.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




