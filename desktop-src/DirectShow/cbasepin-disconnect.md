---
description: 'CBasePin.Disconnect-Methode: Die Disconnect-Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die IPin::D isconnect-Methode.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: CBasePin.Disconnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0048624b79daa6948851fd9a56142b97c7e185caa9bbcbdeb6c2c1b19f591eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916630"
---
# <a name="cbasepindisconnect-method"></a>CBasePin.Disconnect-Methode

Die `Disconnect` -Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die [**IPin::D isconnect-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Syntax


```C++
HRESULT Disconnect();
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

Die Basisklasse delegiert den Großteil der Arbeit an die [**CBasePin::D isconnectInternal-Methode.**](cbasepin-disconnectinternal.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




