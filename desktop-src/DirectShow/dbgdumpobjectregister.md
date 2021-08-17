---
description: Die DbgDumpObjectRegister-Funktion zeigt Informationen zu aktiven Objekten an. Wird in Einzelhandels-Builds ignoriert.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: DbgDumpObjectRegister-Funktion (Wxdebug.h)
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
ms.openlocfilehash: d82d7b419949210e19460880126a07ad52f63ae59f6055e5a2b968a2dd5c7beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821577"
---
# <a name="dbgdumpobjectregister-function"></a>DbgDumpObjectRegister-Funktion

Die `DbgDumpObjectRegister` Funktion zeigt Informationen zu aktiven Objekten an. Wird in Einzelhandels-Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In Debugbuilds verwaltet die Debugbibliothek eine Liste aktiver Objekte. Die Liste enthält alle Objekte, die von [**CBaseObject**](cbaseobject.md)abgeleitet sind, vom aktuellen Modul erstellt wurden und nicht zerstört wurden. Die **CBaseObject-Konstruktor-** und Destruktormethoden aktualisieren die Liste.

Diese Funktion generiert mehrere LOG \_ MEMORY-Meldungen. Auf Protokollierebene 1 zeigt die Funktion nur die Gesamtzahl der Objekte an. Auf Protokollierebene 2 oder höher wird eine Liste der Objekte angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




