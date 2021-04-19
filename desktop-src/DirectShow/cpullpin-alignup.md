---
description: Die alignup-Methode rundet einen Wert auf eine angegebene Ausrichtungs Grenze. Beachten Sie, dass in Windows 7 entfernt wurde. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Cpullpin. alignup-Methode (pullpin. h)
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
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370719"
---
# <a name="cpullpinalignup-method"></a>Cpullpin. alignup-Methode

Die **alignup** -Methode rundet einen Wert auf eine angegebene Ausrichtungs Grenze.

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

*ll* 
</dt> <dd>

Gibt die Zahl an, die ausgerichtet werden soll.

</dd> <dt>

*lalign* 
</dt> <dd>

Gibt die Ausrichtungs Grenze an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das ausgerichtete Ergebnis zurück.

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Diese Methode kann einen numerischen Überlauf verursachen, wenn *ll* + (*lalign* -1) überläuft.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




