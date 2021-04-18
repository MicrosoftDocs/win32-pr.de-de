---
description: Mit der removepin-Methode wird eine angegebene PIN aus dem Filter entfernt. Die-Methode löscht die PIN nicht.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: CSource. removepin-Methode (Quelle. h)
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
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361010"
---
# <a name="csourceremovepin-method"></a>CSource. removepin-Methode

Mit der- `RemovePin` Methode wird eine angegebene PIN aus dem Filter entfernt. Die-Methode löscht die PIN nicht.

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

Zeiger auf das [**csourcestream**](csourcestream.md) -Objekt, das die PIN implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Der Filter enthält diese PIN nicht.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die dekonstruktormethode ruft diese Methode auf, um die Ausgabe-PIN aus dem Filter zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




