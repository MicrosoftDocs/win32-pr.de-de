---
description: Die Funktion "ccheapfree" gibt den von der Funktion "cbillizuzuordnungs" zugeordneten Speicher frei.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Ccheapfree-Funktion (Netmon. h)
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
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131860"
---
# <a name="ccheapfree-function"></a>Ccheapfree-Funktion

Die Funktion " **ccheapfree** " gibt den von der Funktion " **cbillizuzuordnungs** " zugeordneten Speicher frei.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmem* 
</dt> <dd>

Zeiger auf den Arbeitsspeicher, der von dieser Funktion freigegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die **ccheapfree** -Funktion erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Setccinstptr](setccinstptr.md)
</dt> <dt>

[Getccinstptr](getccinstptr.md)
</dt> <dt>

[Ccheap-Zuweisung](ccheapalloc.md)
</dt> <dt>

[Ccheaprezuweisung](ccheaprealloc.md)
</dt> <dt>

[Ccheapsize](ccheapsize.md)
</dt> </dl>

 

 




