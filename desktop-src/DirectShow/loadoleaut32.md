---
description: Die LoadOLEAut32-Funktion lädt die Automation Dynamic-Link Library (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: LoadOLEAut32-Funktion (ComBase. h)
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
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369949"
---
# <a name="loadoleaut32-function"></a>LoadOLEAut32-Funktion

Die **LoadOLEAut32** -Funktion lädt die Automation Dynamic-Link Library (OleAut32.dll).

## <a name="syntax"></a>Syntax


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für eine Automation-dll-Instanz zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der [**cbaseobject-debugtor**](cbaseobject.md) das Objekt zerstört, das OleAut32.dll geladen hat, wird die Bibliothek entladen, wenn Sie noch geladen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> </dl>

 

 




