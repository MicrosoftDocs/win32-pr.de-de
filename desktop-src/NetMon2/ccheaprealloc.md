---
description: Die ccheaprebelegc-Funktion ordnet den von der ccheapbelegc-Funktion zugewiesenen Arbeitsspeicher neu zu.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Ccheaprezuweisung-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756451"
---
# <a name="ccheaprealloc-function"></a>Ccheaprezuweisung-Funktion

Die **ccheaprebelegc** -Funktion ordnet den von der **ccheapbelegc** -Funktion zugewiesenen Arbeitsspeicher neu zu.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmem* 
</dt> <dd>

Zeiger auf den ursprünglich zugeordneten Arbeitsspeicher.

</dd> <dt>

*dwBytes* 
</dt> <dd>

Größe des neu belegten Speichers (gemessen in Bytes).

</dd> <dt>

*bzeroinit* 
</dt> <dd>

Indikator dafür, ob neu zugeordneter Speicher initialisiert wurde. Wenn der Parameterwert **true** ist, wird der neu zugewiesene Speicher mit 0 (null) initialisiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den neu zugeordneten Speicher.

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

[Ccheapsize](ccheapsize.md)
</dt> </dl>

 

 




