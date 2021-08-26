---
description: 'CBaseOutputPin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: CBaseOutputPin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0600402301bf416dc0863c4ccff05cac698ec53871b03fd8a84f3873fd43163a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983420"
---
# <a name="cbaseoutputpininactive-method"></a>CBaseOutputPin.Inactive-Methode

Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                          | Beschreibung                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                          |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Es ist keine Speicherzuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::Inactive-Methode.**](cbasepin-inactive.md) Sie ruft die [**IMemAllocator::D commit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) auf, um die Speicherbelegung zu decommitieren.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




