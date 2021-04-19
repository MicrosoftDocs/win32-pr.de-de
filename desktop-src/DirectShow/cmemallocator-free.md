---
description: Die Free-Methode wird während eines Decommit-Vorgangs aufgerufen.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Cmemzuzucator. Free-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362147"
---
# <a name="cmemallocatorfree-method"></a>Cmemzuzucator. Free-Methode

Die- `Free` Methode wird während eines Decommit-Vorgangs aufgerufen. Diese Methode implementiert die reine virtuelle [**cbasezuordcator:: Free**](cbaseallocator-free.md) -Methode, bewirkt aber nichts. Der Puffer Arbeitsspeicher wird erst freigegeben, wenn das **cmemzuordcator** -Objekt zerstört wird. Die dekonstruktormethode ruft [**cmembelegcator:: reallyfree**](cmemallocator-reallyfree.md) auf, um den Arbeitsspeicher freizugeben.

## <a name="syntax"></a>Syntax


```C++
void Free();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmemzuordcator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




