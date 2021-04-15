---
description: Die setccinstptr-Funktion erfasst einen Kontext Instanz-Zeiger.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Setccinstptr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526753"
---
# <a name="setccinstptr-function"></a>Setccinstptr-Funktion

Die **setccinstptr** -Funktion erfasst einen Kontext Instanz-Zeiger.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpcurrcaptureinst* 
</dt> <dd>

Zeiger auf die der Erfassung hinzugefügten Instanzdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um einen Zeiger auf einen Block zu speichern, der mit der **ccheap-Zuordnungs** Funktion zugeordnet wurde. Jeder Parser kann eine einzelne Instanz der Daten für eine Erfassung festlegen.

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

[Getccinstptr](getccinstptr.md)
</dt> <dt>

[Ccheap-Zuweisung](ccheapalloc.md)
</dt> <dt>

[Ccheapfree](ccheapfree.md)
</dt> <dt>

[Ccheaprezuweisung](ccheaprealloc.md)
</dt> <dt>

[Ccheapsize](ccheapsize.md)
</dt> </dl>

 

 




