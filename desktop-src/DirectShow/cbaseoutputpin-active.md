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
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096208"
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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::Active-Methode.**](cbasepin-active.md) Sie ruft die [**IMemAllocator::Commit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) für die Zuweisung auf, um Speicher für Puffer zu reservieren.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




