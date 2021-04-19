---
description: Die EndOfStream-Methode benachrichtigt den Filter, dass die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms erhalten hat.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Cbaserderderer. EndOf Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364762"
---
# <a name="cbaserendererendofstream-method"></a>Cbaserderderer. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt den Filter, dass die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms erhalten hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie eine Benachrichtigung über das Ende des Datenstroms empfängt.

Diese Methode legt das Flag " [**cbaserrederer:: m \_ BeOS**](cbaserenderer-m-beos.md) " auf " **true** " fest und ruft die [**cbasererentiderer:: sendendofstream**](cbaserenderer-sendendofstream.md) -Methode auf, um ein [**EC \_ Complete**](ec-complete.md) -Ereignis zu planen. Wenn der Filter angehalten wurde und auf eine Stichprobe wartet, schließt diese Methode den Zustandsübergang ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




