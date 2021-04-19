---
description: Die forceRefresh-Methode ist veraltet.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Cpospassthru. forceRefresh-Methode (ctlutil. h)
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
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372122"
---
# <a name="cpospassthruforcerefresh-method"></a>Cpospassthru. forceRefresh-Methode

Die- `ForceRefresh` Methode ist veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Ursprünglich war diese Klasse so konzipiert, dass Zeiger auf die Schnittstellen [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) der verbundenen Pin zwischengespeichert werden. Die- `ForceRefresh` Methode hat diese Schnittstellen freigegeben.

Wie momentan implementiert, speichert diese Klasse diese Schnittstellen nicht zwischen. Aus Kompatibilitätsgründen `ForceRefresh` ist die Methode weiterhin enthalten, aber Sie gibt "OK" zurück, \_ ohne etwas zu tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




