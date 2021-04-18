---
description: Die Disconnect-Methode unterbricht die aktuelle PIN-Verbindung. Diese Methode implementiert die IPin::D isconnect-Methode.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Cbasepin. Disconnect-Methode (amfilter. h)
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
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354648"
---
# <a name="cbasepindisconnect-method"></a>Cbasepin. Disconnect-Methode

Die- `Disconnect` Methode unterbricht die aktuelle PIN-Verbindung. Diese Methode implementiert die [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Disconnect();
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

Die Basisklasse delegiert den größten Teil der Arbeit an die [**cbasepin::D isconnectinternal**](cbasepin-disconnectinternal.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




