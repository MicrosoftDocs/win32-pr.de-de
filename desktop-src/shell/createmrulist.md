---
description: Erstellt eine neue Liste der zuletzt verwendeten (MRU).
title: Funktion "anatemrulistw"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750248"
---
# <a name="createmrulistw-function"></a>Funktion "anatemrulistw"

Erstellt eine neue Liste der zuletzt verwendeten (MRU).

## <a name="syntax"></a>Syntax


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmi* \[ in\]
</dt> <dd>

Typ: **lpmruinfo**

Ein Zeiger auf eine [**mruinfo**](mruinfo.md) -Struktur, die die MRU-Liste definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt ein Handle für die neue MRU-Liste oder bei einem Fehler 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten. Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 400 für " **featemrulistw**" ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | " **Anatemrulistw** " (Unicode)<br/>                                                                        |



 

 
