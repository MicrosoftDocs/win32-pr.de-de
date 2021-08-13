---
description: Aktiviert oder deaktiviert die Debugprotokollierung eines bestimmten kritischen Abschnitts.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: DbgLockTrace-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b55736b2efb8fd4cfbca40710caa930c200c84e1ceec9c8c4f7439468c1add1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654070"
---
# <a name="dbglocktrace-function"></a>DbgLockTrace-Funktion

Aktiviert oder deaktiviert die Debugprotokollierung eines bestimmten kritischen Abschnitts.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcCrit* 
</dt> <dd>

Zeiger auf einen [**kritischen CCritSec-Abschnitt.**](ccritsec.md)

</dd> <dt>

*fTrace* 
</dt> <dd>

Wert, der an gibt, ob die Protokollierung aktiviert ist. Verwenden **Sie TRUE,** um die Protokollierung zu aktivieren, oder **FALSE,** um sie zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, um einen bestimmten kritischen Abschnitt nachverfolgung zu verfolgen. Standardmäßig ist die Debugprotokollierung kritischer Abschnitte aufgrund der großen Anzahl kritischer Abschnitte deaktiviert.

Führen Sie zum Nachverfolgen eines kritischen Abschnitts die folgenden Schritte aus:

1.  Definieren Sie DEBUG oder \_ DEBUG, bevor Sie die DirectShow-Header hinzufügen.
2.  Aktivieren Sie die Debugprotokollierung für kritische Abschnitte, indem [**Sie DbgSetModuleLevel mit**](dbgsetmodulelevel.md) dem LOG \_ LOCKING-Flag aufrufen.
3.  Rufen **Sie DbgLockTrace für** den kritischen Abschnitt auf, den Sie nachverfolgen möchten.

In Einzelhandels-Builds hat **die DbgLockTrace-Funktion** keine Auswirkungen.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie ein kritischer Abschnitt nachverfolgt wird.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Wichtige Funktionen für das Debuggen von Abschnitten](critical-section-debugging-functions.md)
</dt> </dl>

 

 




