---
description: Die RemovePin-Methode entfernt einen angegebenen Pin aus dem Filter. Die -Methode löscht den Pin nicht.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: CSource.RemovePin-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 376c2b292b0bdba9a79593c8264ecce17b916a88cfd49407638d637d1fbda6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767840"
---
# <a name="csourceremovepin-method"></a>CSource.RemovePin-Methode

Die `RemovePin` -Methode entfernt einen angegebenen Pin aus dem Filter. Die -Methode löscht den Pin nicht.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStream* 
</dt> <dd>

Zeiger auf das [**CSourceStream-Objekt,**](csourcestream.md) das den Pin implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Filter enthält diesen Pin nicht.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Destruktormethode ruft diese Methode auf, um den Ausgabepin aus dem Filter zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




