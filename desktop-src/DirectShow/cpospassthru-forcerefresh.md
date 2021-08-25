---
description: Die ForceRefresh-Methode ist veraltet.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: CPosPassThru.ForceRefresh-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915520"
---
# <a name="cpospassthruforcerefresh-method"></a>CPosPassThru.ForceRefresh-Methode

Die `ForceRefresh` -Methode ist veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Ursprünglich wurde diese Klasse entwickelt, um Zeiger auf die [**IMediaPosition-**](/windows/desktop/api/Control/nn-control-imediaposition) und IMediaSeeking-Schnittstellen des verbundenen [**Pins zwischenspeichern.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Die `ForceRefresh` -Methode hat diese Schnittstellen freigegeben.

Wie derzeit implementiert, speichert diese Klasse diese Schnittstellen nicht zwischen. Aus Kompatibilitätsgef noch immer ist die -Methode enthalten, gibt aber `ForceRefresh` "S \_ OK" zurück, ohne etwas zu tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




