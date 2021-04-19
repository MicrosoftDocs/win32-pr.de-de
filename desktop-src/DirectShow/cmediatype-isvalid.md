---
description: Die IsValid-Methode bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Cmediatype. IsValid-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367713"
---
# <a name="cmediatypeisvalid-method"></a>Cmediatype. IsValid-Methode

Die- `IsValid` Methode bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn diesem Objekt ein Haupttyp zugewiesen wurde. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

[**Cmediatype**](cmediatype.md) -Objekte werden standardmäßig mit einem Haupttyp von GUID NULL initialisiert \_ . Ruft diese Methode auf, um zu bestimmen, ob das Objekt ordnungsgemäß initialisiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




