---
description: 'CBaseOutputPin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: CBaseOutputPin.Active-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94e71b3a85fdddd3ea4554575b07871ecdc09070f00c988f24f31378e9effb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640030"
---
# <a name="cbaseoutputpinactive-method"></a>CBaseOutputPin.Active-Methode

Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                          | Beschreibung                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Es ist keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::Active-Methode.**](cbasepin-active.md) Sie ruft die [**IMemAllocator::Commit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) für die Zuweisung auf, um Speicher für Puffer zu reservieren.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




