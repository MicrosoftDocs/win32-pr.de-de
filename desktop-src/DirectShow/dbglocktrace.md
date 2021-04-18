---
description: Aktiviert oder deaktiviert die Debugprotokollierung eines bestimmten kritischen Abschnitts.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Dbglocktrace-Funktion (wxutil. h)
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
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352963"
---
# <a name="dbglocktrace-function"></a>Dbglocktrace-Funktion

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

*pccrit* 
</dt> <dd>

Zeiger auf einen kritischen [**ccritsec**](ccritsec.md) -Abschnitt.

</dd> <dt>

*Ablaufverfolgungs-* 
</dt> <dd>

Wert, der angibt, ob die Protokollierung aktiviert ist. Verwenden Sie **true** , **um die Protokollierung zu aktivieren** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um einen bestimmten kritischen Abschnitt zu verfolgen. Standardmäßig ist die Debugprotokollierung kritischer Abschnitte aufgrund der großen Anzahl kritischer Abschnitte deaktiviert.

Führen Sie die folgenden Schritte aus, um einen kritischen Abschnitt zu verfolgen:

1.  Definieren Sie Debug oder \_ Debug, bevor Sie die DirectShow-Header einschließen.
2.  Aktivieren Sie die Debugprotokollierung für kritische Abschnitte, indem Sie [**dbgsetmodulelevel**](dbgsetmodulelevel.md) mit dem Protokoll \_ Sperr Flag aufrufen.
3.  Nennen Sie **dbglocktrace** im kritischen Abschnitt, den Sie verfolgen möchten.

In Einzelhandels Builds hat die **dbglocktrace** -Funktion keine Auswirkungen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie ein kritischer Abschnitt verfolgt wird.


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
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kritische Abschnitts Debuggingfunktionen](critical-section-debugging-functions.md)
</dt> </dl>

 

 




