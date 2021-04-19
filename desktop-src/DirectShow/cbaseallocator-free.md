---
description: Die Free-Methode gibt den gesamten Puffer Arbeitsspeicher frei. Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung aufhebt, nachdem das letzte Medien Beispiel freigegeben wurde.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Cbasezucator. Free-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361925"
---
# <a name="cbaseallocatorfree-method"></a>Cbasezucator. Free-Methode

Die- `Free` Methode gibt den gesamten Puffer Arbeitsspeicher frei. Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung aufhebt, nachdem das letzte Medien Beispiel freigegeben wurde.

## <a name="syntax"></a>Syntax


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachdem die [**Decommit**](cbaseallocator-decommit.md) -Methode aufgerufen wurde, ruft die Zuweisung diese Methode auf, wenn Sie das letzte Medien Beispiel freigibt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




