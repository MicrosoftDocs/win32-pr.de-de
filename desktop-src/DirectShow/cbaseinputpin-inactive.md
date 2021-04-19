---
description: Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Cbasinputpin. inaktive Methode (amfilter. h)
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
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369600"
---
# <a name="cbaseinputpininactive-method"></a>Cbasinputpin. inaktive Methode

Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                          | Beschreibung                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                          |
| <dl> <dt>**VFW \_ E \_ No- \_ Zuweisung**</dt> </dl> | Es ist keine Speicherzuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode. Sie ruft die [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) -Methode auf, um die Speicher Belegung zu Decommit.

Wenn Sie diese Methode überschreiben, müssen Sie die Basisklassen Methode aus der über schreibenden Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




