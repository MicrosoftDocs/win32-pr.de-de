---
description: 'CDynamicOutputPin.Disconnect-Methode: Die Disconnect-Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die IPin::D isconnect-Methode.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: CDynamicOutputPin.Disconnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099298"
---
# <a name="cdynamicoutputpindisconnect-method"></a>CDynamicOutputPin.Disconnect-Methode

Die `Disconnect` -Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die [**IPin::D isconnect-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Syntax


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                             | Beschreibung                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die Stecknadel wurde nicht verbunden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::D isconnect-Methode,**](cbasepin-disconnect.md) um das Trennen der Verbindung zu aktivieren, während der Filter aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




