---
description: Gibt das handle frei, das der LISTE der zuletzt verwendeten (MRU) zugeordnet ist, und schreibt zwischengespeicherte Daten in die Registrierung.
title: FreeMRUList-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840621"
---
# <a name="freemrulist-function"></a>FreeMRUList-Funktion

Gibt das handle frei, das der LISTE der zuletzt verwendeten (MRU) zugeordnet ist, und schreibt zwischengespeicherte Daten in die Registrierung.

## <a name="syntax"></a>Syntax


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMRU* \[ In\]
</dt> <dd>

Typ: **HANDLE**

Das Handle der frei zu gebenden MRU-Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt bei Erfolg einen nicht negativen Wert zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Wenn die MRU-Liste mit dem **MRU \_ CACHEWRITE-Flag** erstellt wurde, bewirkt der Aufruf von **FreeMRUList,** dass alle Änderungen, die noch nicht in die Version der in der Registrierung gespeicherten MRU-Liste geschrieben wurden, zu diesem Zeitpunkt geschrieben werden.

Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten. Es muss aus der Ordnungszahl comctl32.dll 152 extrahiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 




