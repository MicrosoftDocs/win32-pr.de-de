---
description: Die CCHeapFree-Funktion gibt den von der CCHeapAlloc-Funktion zugeordneten Arbeitsspeicher frei.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: CCHeapFree-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b29d57c3d56136103fb1948340472343f56727c2df0268a5036dc148fdd0493a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796340"
---
# <a name="ccheapfree-function"></a>CCHeapFree-Funktion

Die **CCHeapFree-Funktion** gibt den von der **CCHeapAlloc-Funktion zugeordneten Arbeitsspeicher** frei.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpMem* 
</dt> <dd>

Zeiger auf den Arbeitsspeicher, den diese Funktion frei gibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die **CCHeapFree-Funktion** erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




