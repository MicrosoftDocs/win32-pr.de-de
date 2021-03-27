---
description: Registriert eine Fenster Klasse, mit der das allgemeine Syslink-Steuerelement in einem Fenster verwendet werden kann.
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
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980024"
---
# <a name="linkwindow_registerclass-function"></a>Linkwindow- \_ registerClass-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar. Verwenden Sie stattdessen [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]

Registriert eine Fenster Klasse, mit der das allgemeine [Syslink](../controls/syslink-overview.md) -Steuerelement in einem Fenster verwendet werden kann.

## <a name="syntax"></a>Syntax


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt **true** zurück, wenn die Registrierung erfolgreich war. Andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss. Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen Shell32.dll, um ein Modul Handle abzurufen. Dann rufe Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordinalzahl 258 auf, um diese Funktion zu verwenden.

Verwenden Sie [**linkwindow \_ unregisterclass**](linkwindow-unregisterclass.md) , um die Registrierung der Klasse nach der Verwendung aufzuheben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Syslink-Steuerelemente](../controls/syslink-overview.md)
</dt> </dl>

 

 
