---
description: Die LoadOLEAut32-Funktion lädt die Dynamic Link Library (OleAut32.dll) von Automation.
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: LoadOLEAut32-Funktion (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502310"
---
# <a name="loadoleaut32-function"></a>LoadOLEAut32-Funktion

Die **LoadOLEAut32-Funktion** lädt die Dynamic Link Library (OleAut32.dll) von Automation.

## <a name="syntax"></a>Syntax


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für eine Automation DLL-Instanz zurück.

## <a name="remarks"></a>Hinweise

Wenn der [**CBaseObject-Destruktor**](cbaseobject.md) das Objekt zerstört, das OleAut32.dll geladen hat, wird die Bibliothek entladen, wenn sie noch geladen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> </dl>

 

 




