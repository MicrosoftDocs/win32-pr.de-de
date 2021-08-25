---
description: Die DisconnectInternal-Methode unterbricht die aktuelle Pinverbindung.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: CBasePin.DisconnectInternal-Methode (Amfilter.h)
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
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916530"
---
# <a name="cbasepindisconnectinternal-method"></a>CBasePin.DisconnectInternal-Methode

Die `DisconnectInternal` -Methode unterbricht die aktuelle Pinverbindung.

## <a name="syntax"></a>Syntax


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                         | Beschreibung                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Die Stecknadel wurde nicht verbunden.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NICHT \_ BEENDET**</dt> </dl> | Der Filter ist aktiv, und der Pin unterstützt keine dynamische wiederhergestellte Verbindung.<br/> |



 

## <a name="remarks"></a>Hinweise

Die [**CBasePin::D isconnect-Methode**](cbasepin-disconnect.md) delegiert den Disconnect-Prozess an diese Methode. Diese Methode ruft die [**CBasePin::BreakConnect-Methode**](cbasepin-breakconnect.md) auf. Außerdem wird die Verweisanzahl für den anderen Pin frei, der von der [**CBasePin::m \_ Connected-Membervariablen**](cbasepin-m-connected.md) gehalten wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




