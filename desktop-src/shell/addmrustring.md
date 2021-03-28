---
description: Fügt am Anfang der Liste der zuletzt verwendeten (MRU) eine Zeichenfolge hinzu.
title: Addmrustringw-Funktion
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041618"
---
# <a name="addmrustringw-function"></a>Addmrustringw-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar. \]

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

*hmru* \[ in\]
</dt> <dd>

Typ: **handle**

Das Handle der MRU-Liste.

</dd> <dt>

*szString* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf die Daten. Dabei kann es sich entweder um eine Zeichenfolge handeln oder, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, Binärdaten. Im Fall von Binärdaten gibt das erste **DWORD** die Größe an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt bei erfolgreicher Ausführung einen nicht negativen Wert zurück, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten. Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 401 für **addmrustringw** ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Addmrustringw** (Unicode)<br/>                                                                         |



 

