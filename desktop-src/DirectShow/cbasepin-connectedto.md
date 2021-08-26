---
description: Die ConnectedTo-Methode ruft ggf. einen Zeiger auf den verbundenen Pin ab. Diese Methode implementiert die IPin::ConnectedTo-Methode.
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: CBasePin.ConnectedTo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a37eafe9abf226be20cf5d573abc91bc52ee070e7667dbab3a8799f74022c92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916760"
---
# <a name="cbasepinconnectedto-method"></a>CBasePin.ConnectedTo-Methode

Die `ConnectedTo` -Methode ruft ggf. einen Zeiger auf den verbundenen Pin ab. Diese Methode implementiert die [**IPin::ConnectedTo-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="syntax"></a>Syntax


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppPin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                           | Beschreibung                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeigerargument.**<br/> |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Pin ist nicht verbunden.<br/>      |



 

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich ist, verfügt die **zurückgegebene IPin-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




