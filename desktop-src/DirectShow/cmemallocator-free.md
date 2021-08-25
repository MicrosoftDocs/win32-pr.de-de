---
description: Die Free-Methode wird während eines Decommit-Vorgangs aufgerufen.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: CMemAllocator.Free-Methode (Amfilter.h)
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
ms.openlocfilehash: 2c2ffea6fdd60e4053f6c00ee1c87ca9596560909864c861d46b5728dad13a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155992"
---
# <a name="cmemallocatorfree-method"></a>CMemAllocator.Free-Methode

Die `Free` -Methode wird während eines Decommit-Vorgangs aufgerufen. Diese Methode implementiert die reine virtuelle [**CBaseAllocator::Free-Methode,**](cbaseallocator-free.md) führt jedoch keine Maßnahmen aus. Der Pufferspeicher wird erst freigegeben, wenn das **CMemAllocator-Objekt** zerstört wurde. Die Destruktormethode ruft [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) auf, um den Arbeitsspeicher freizugeben.

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
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMemAllocator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




