---
description: 'Die Skip-Methode überspringt eine angegebene Anzahl von Medientypen. Diese Methode implementiert die ienummediatypes:: Skip-Methode.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Cenumschlag mediatypes. Skip-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354665"
---
# <a name="cenummediatypesskip-method"></a>Cenumschlag mediatypes. Skip-Methode

Die- `Skip` Methode überspringt eine angegebene Anzahl von Medientypen. Diese Methode implementiert die [**ienummediatypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cmediatypes* 
</dt> <dd>

Anzahl der zu über springenden Medientypen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Wird über das Ende der Sequenz übersprungen.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt> </dl> | Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenum mediatypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




