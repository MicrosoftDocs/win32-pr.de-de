---
description: Die IsValid-Methode bestimmt, ob diesem Objekt ein Haupttyp zugewiesen wurde.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: CMediaType.IsValid-Methode (Mtype.h)
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
ms.openlocfilehash: 3611d36cfe19623840f102b820b2b312138b1e116d32fc399927da57e7f47300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016262"
---
# <a name="cmediatypeisvalid-method"></a>CMediaType.IsValid-Methode

Die `IsValid` -Methode bestimmt, ob diesem Objekt ein Haupttyp zugewiesen wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn diesem Objekt ein Haupttyp zugewiesen wurde. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Standardmäßig werden [**CMediaType-Objekte**](cmediatype.md) mit einem Haupttyp von GUID \_ NULL initialisiert. Rufen Sie diese Methode auf, um zu bestimmen, ob das Objekt ordnungsgemäß initialisiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




