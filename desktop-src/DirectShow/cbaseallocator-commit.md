---
description: Die Commit-Methode weist den Arbeitsspeicher für die Puffer zu. Diese Methode implementiert die IMemAllocator::Commit-Methode.
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: CBaseAllocator.Commit-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087580"
---
# <a name="cbaseallocatorcommit-method"></a>CBaseAllocator.Commit-Methode

Die `Commit` -Methode weist den Arbeitsspeicher für die Puffer zu. Diese Methode implementiert die [**IMemAllocator::Commit-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)

## <a name="syntax"></a>Syntax


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind diese in der folgenden Liste.



| Rückgabecode                                                                                       | Beschreibung                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Pufferanforderungen wurden nicht angegeben.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Aufrufen dieser Methode die [**CBaseAllocator::SetProperties-Methode**](cbaseallocator-setproperties.md) auf, um die Pufferanforderungen anzugeben.

Diese Methode ruft die virtuelle Methode [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) auf, um den Arbeitsspeicher für die Puffer zu reservieren. Abgeleitete Klassen können **Alloc überschreiben.** Wenn ein Decommitvorgang aussteht, wird er abgebrochen.

Sie müssen diese Methode aufrufen, bevor Sie [**die CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




