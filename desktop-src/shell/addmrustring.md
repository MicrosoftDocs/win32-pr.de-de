---
description: Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.
title: AddMRUStringW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 4ac72c44b670466f10cd708b81b1a84f93a349afcb0d81473ed5e6578c20617a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861592"
---
# <a name="addmrustringw-function"></a>AddMRUStringW-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows. \]

Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.

## <a name="syntax"></a>Syntax


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMRU* \[ In\]
</dt> <dd>

Typ: **HANDLE**

Das Handle der MRU-Liste.

</dd> <dt>

*szString* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf die Daten. Dies kann entweder eine Zeichenfolge oder, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde, binäre Daten sein. Im Fall von Binärdaten gibt das erste **DWORD** seine Größe an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt bei Erfolg einen nicht negativen Wert zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten. Auf sie kann über [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) zugegriffen oder aus comctl32.dll durch ihre Ordnungszahl extrahiert werden, die 401 für **AddMRUStringW ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

