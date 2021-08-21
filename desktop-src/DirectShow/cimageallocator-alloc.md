---
description: Die Alloc-Methode weist Den Puffern Arbeitsspeicher zu. Diese Methode überschreibt die CBaseAllocator::Alloc-Methode.
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: CImageAllocator.Alloc-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bdf4c36bcf66d46a5c5ee7df16ac04a4461bd3a88de91e175b81e89ce496e1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076240"
---
# <a name="cimageallocatoralloc-method"></a>CImageAllocator.Alloc-Methode

Die `Alloc` -Methode weist Den Puffern Arbeitsspeicher zu. Diese Methode überschreibt die [**CBaseAllocator::Alloc-Methode.**](cbaseallocator-alloc.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird von der [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen, wenn der Filter einen Commit für die Zuweisung vorsord.

Diese Methode erstellt eine Liste von Medienbeispielen, die als [**CImageSample-Objekte implementiert**](cimagesample.md) werden. Jedes Beispiel enthält eine geräteunabhängige GDI-Bitmap mithilfe der GDI **CreateDIBSection-Funktion.**

Intern ruft diese Methode [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) auf, um jedes DIB zu erstellen, und [**CImageAllocator::CreateImageSample,**](cimageallocator-createimagesample.md) um jedes Beispiel zu erstellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageAllocator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




