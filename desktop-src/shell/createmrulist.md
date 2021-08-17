---
description: Erstellt eine neue LISTE der zuletzt verwendeten (MRU).
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
ms.openlocfilehash: e5f97d1f50dae081eac00014415129d8a4c858a0e6e2c3406e1a6c4f6905c71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861397"
---
# <a name="createmrulistw-function"></a>CreateMRUListW-Funktion

Erstellt eine neue LISTE der zuletzt verwendeten (MRU).

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

Gibt ein Handle für die neue MRU-Liste oder bei einem Fehler 0 zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten. Auf sie kann über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zugegriffen oder aus comctl32.dll durch ihre Ordnungszahl extrahiert werden, die 400 für **CreateMRUListW ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
