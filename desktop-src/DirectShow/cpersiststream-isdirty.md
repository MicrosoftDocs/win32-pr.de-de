---
description: Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Cpersiststream. IsDirty-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370130"
---
# <a name="cpersiststreamisdirty-method"></a>Cpersiststream. IsDirty-Methode

Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn der Filter gespeichert werden muss, und s \_ false, wenn er nicht gespeichert werden muss.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die **IPersistStream:: IsDirty** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




