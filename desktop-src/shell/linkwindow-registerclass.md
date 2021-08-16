---
description: Registriert eine Fensterklasse, die die Verwendung des allgemeinen SysLink-Steuerelements in einem Fenster ermöglicht.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 75936c918a930698ef803b02743b935660e876b0d87d7f6d5eddce91d4f4c0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968959"
---
# <a name="linkwindow_registerclass-function"></a>LinkWindow \_ RegisterClass-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Er kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [**InitCommonControlsEx.**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex)\]

Registriert eine Fensterklasse, die die Verwendung des allgemeinen [SysLink-Steuerelements](../controls/syslink-overview.md) in einem Fenster ermöglicht.

## <a name="syntax"></a>Syntax


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Gibt **TRUE** zurück, wenn die Registrierung erfolgreich war. **Andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist kein Header oder eine Bibliotheksdatei zugeordnet, daher muss sie als Ordinalwert aufgerufen werden. Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen Shell32.dll auf, um ein Modulhandle abzurufen. Rufen Sie dann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modulhandle und der Ordnungszahl 258 auf, um diese Funktion zu verwenden.

Verwenden Sie [**LinkWindow \_ UnregisterClass,**](linkwindow-unregisterclass.md) um die Registrierung der Klasse nach der Verwendung zu aufheben.

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

 

 
