---
description: Gibt das der zuletzt verwendeten (MRU)-Liste zugeordnete Handle frei und schreibt zwischengespeicherte Daten in die Registrierung.
title: Freemrulist-Funktion
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979649"
---
# <a name="freemrulist-function"></a>Freemrulist-Funktion

Gibt das der zuletzt verwendeten (MRU)-Liste zugeordnete Handle frei und schreibt zwischengespeicherte Daten in die Registrierung.

## <a name="syntax"></a>Syntax


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmru* \[ in\]
</dt> <dd>

Typ: **handle**

Das Handle der MRU-Liste, die freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt bei erfolgreicher Ausführung einen nicht negativen Wert zurück, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Wenn die MRU-Liste mit dem **MRU \_ cachewrite** -Flag erstellt wurde, bewirkt das Aufrufen von **freemrulist** , dass alle Änderungen, die noch nicht in die in der Registrierung gespeicherte Version der MRU-Liste geschrieben wurden, zu diesem Zeitpunkt geschrieben werden.

Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten. Sie muss aus comctl32.dll durch die Ordnungszahl 152 extrahiert werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 




