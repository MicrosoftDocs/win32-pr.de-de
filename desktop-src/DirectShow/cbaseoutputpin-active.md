---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Cbaseoutputpin. Active-Methode (amfilter. h)
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
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365496"
---
# <a name="cbaseoutputpinactive-method"></a>Cbaseoutputpin. Active-Methode

Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                          | Beschreibung                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                   |
| <dl> <dt>**VFW \_ E \_ No- \_ Zuweisung**</dt> </dl> | Es ist keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: Active**](cbasepin-active.md) -Methode. Es wird die [**imemallocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) -Methode für die Zuweisung aufgerufen, um Speicher für Puffer zuzuweisen.

Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




