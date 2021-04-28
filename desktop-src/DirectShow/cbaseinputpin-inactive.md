---
description: 'CBaseInputPin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: CBaseInputPin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1324e9e2641e5e05bc3b0429ee269098c13d4bae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099728"
---
# <a name="cbaseinputpininactive-method"></a>CBaseInputPin.Inactive-Methode

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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::Inactive-Methode.**](cbasepin-inactive.md) Sie ruft die [**IMemAllocator::D ecommit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) auf, um denCommit der Speicherbelegung zu decommitieren.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




