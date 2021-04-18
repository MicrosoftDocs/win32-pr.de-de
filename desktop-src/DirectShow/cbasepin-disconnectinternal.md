---
description: Die disconnectinternal-Methode unterbricht die aktuelle PIN-Verbindung.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Cbasepin. disconnectinternal-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364772"
---
# <a name="cbasepindisconnectinternal-method"></a>Cbasepin. disconnectinternal-Methode

Die- `DisconnectInternal` Methode unterbricht die aktuelle PIN-Verbindung.

## <a name="syntax"></a>Syntax


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                         | Beschreibung                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Die PIN war nicht verbunden.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl> | Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die [**cbasepin::D isconnect**](cbasepin-disconnect.md) -Methode delegiert den Disconnect-Prozess an diese Methode. Diese Methode ruft die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf. Außerdem wird der Verweis Zähler für die andere Pin freigegeben, die von der in [**cbasepin:: m \_ verbundenen**](cbasepin-m-connected.md) Member-Variable gehalten wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




