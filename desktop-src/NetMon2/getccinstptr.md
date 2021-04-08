---
description: Die getccinstptr-Funktion gibt den Zeiger auf die Instanzdaten zurück, die dem Aufzeichnungs Kontext hinzugefügt wurden.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Getccinstptr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750089"
---
# <a name="getccinstptr-function"></a>Getccinstptr-Funktion

Die **getccinstptr** -Funktion gibt den Zeiger auf die Instanzdaten zurück, die dem Aufzeichnungs Kontext hinzugefügt wurden.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf die Instanzdaten einer bestimmten Erfassung.

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

[Ccheap-Zuweisung](ccheapalloc.md)
</dt> <dt>

[Ccheapfree](ccheapfree.md)
</dt> <dt>

[Ccheaprezuweisung](ccheaprealloc.md)
</dt> <dt>

[Ccheapsize](ccheapsize.md)
</dt> </dl>

 

 




