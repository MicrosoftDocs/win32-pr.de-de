---
description: 'Die connectedto-Methode ruft ggf. einen Zeiger auf die verbundene Pin ab. Diese Methode implementiert die IPin:: connectedto-Methode.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Cbasepin. connectedto-Methode (amfilter. h)
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
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354171"
---
# <a name="cbasepinconnectedto-method"></a>Cbasepin. connectedto-Methode

Die- `ConnectedTo` Methode ruft ggf. einen Zeiger auf die verbundene Pin ab. Diese Methode implementiert die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pppin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeigerargument.<br/> |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **IPin** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




