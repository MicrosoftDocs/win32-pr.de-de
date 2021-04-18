---
description: Die ccheapsize-Funktion gibt die Größe des Arbeitsspeichers zurück, der von der ccheap-Zuordnungs Funktion belegt wird.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Ccheapsize-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358562"
---
# <a name="ccheapsize-function"></a>Ccheapsize-Funktion

Die **ccheapsize** -Funktion gibt die Größe des Arbeitsspeichers zurück, der von der **ccheap-Zuordnungs** Funktion belegt wird.

## <a name="syntax"></a>Syntax


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmem* 
</dt> <dd>

Zeiger auf zugewiesenen Speicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Größe des angeforderten Speicherblocks, gemessen in Bytes.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

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

[Ccheapfree](ccheapfree.md)
</dt> <dt>

[Ccheaprezuweisung](ccheaprealloc.md)
</dt> </dl>

 

 




