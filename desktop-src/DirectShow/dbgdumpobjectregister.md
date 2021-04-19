---
description: Die Funktion dbgdumpobjectregiester zeigt Informationen zu aktiven Objekten an. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Dbgdumpobjectregiester-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356453"
---
# <a name="dbgdumpobjectregister-function"></a>Dbgdumpobjectregiester-Funktion

Die- `DbgDumpObjectRegister` Funktion zeigt Informationen zu aktiven Objekten an. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In Debugbuilds verwaltet die Debug-Bibliothek eine Liste aktiver Objekte. Die Liste enthält alle Objekte, die von [**cbaseobject**](cbaseobject.md)abgeleitet sind, vom aktuellen Modul erstellt wurden und nicht zerstört wurden. Der **cbaseobject** -Konstruktor und die dekonstruktormethoden aktualisieren die Liste.

Diese Funktion generiert mehrere Protokoll \_ Speicher Meldungen. Bei der Protokollierungs Stufe 1 zeigt die Funktion nur die Gesamtzahl der Objekte an. In der Protokollierungs Stufe 2 oder höher wird eine Liste der Objekte angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




