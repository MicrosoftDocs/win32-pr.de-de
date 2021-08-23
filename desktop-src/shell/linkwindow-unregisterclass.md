---
description: Aufheben der Registrierung einer Von LinkWindow RegisterClass registrierten \_ Fensterklasse.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968939"
---
# <a name="linkwindow_unregisterclass-function"></a>LinkWindow \_ UnregisterClass-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von geändert oder nicht verfügbar Windows.\]

Aufheben der Registrierung einer Von [**LinkWindow RegisterClass registrierten \_ Fensterklasse.**](linkwindow-registerclass.md)

## <a name="syntax"></a>Syntax


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Gibt **TRUE zurück,** wenn der Vorgang erfolgreich war. **Andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Funktion verfügt nicht über einen zugeordneten Header oder eine Bibliotheksdatei, daher muss sie nach Ordinalwert aufgerufen werden. Rufen [**Sie LoadLibrary mit**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) dem DLL-Namen Shell32.dll, um ein Modulhand handle zu erhalten. Rufen Sie [**dann GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modulhandle und der Ordnungszahl 259 auf, um diese Funktion zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über SysLink-Steuerelemente](../controls/syslink-overview.md)
</dt> </dl>

 

 
