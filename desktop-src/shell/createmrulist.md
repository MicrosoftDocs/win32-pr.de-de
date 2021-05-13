---
description: Erstellt eine neue MRU-Liste (Most Recently Used).
title: CreateMRUListW-Funktion
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
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843381"
---
# <a name="createmrulistw-function"></a>CreateMRUListW-Funktion

Erstellt eine neue MRU-Liste (Most Recently Used).

## <a name="syntax"></a>Syntax


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmi* \[ In\]
</dt> <dd>

Typ: **LPMRUINFO**

Ein Zeiger auf eine [**MRUINFO-Struktur,**](mruinfo.md) die die MRU-Liste definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt ein Handle für die neue MRU-Liste oder 0 (bei einem Fehler) zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten. Der Zugriff kann über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) erfolgen oder aus comctl32.dll durch die Ordnungszahl 400 für **CreateMRUListW** extrahiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
