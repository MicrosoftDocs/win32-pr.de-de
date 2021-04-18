---
description: Hebt die Registrierung einer Fenster Klasse auf, die von linkwindow \_ registerClass registriert wird.
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
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980017"
---
# <a name="linkwindow_unregisterclass-function"></a>Linkwindow \_ unregisterclass-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Hebt die Registrierung einer Fenster Klasse auf, die von [**linkwindow \_ registerClass**](linkwindow-registerclass.md)registriert wird.

## <a name="syntax"></a>Syntax


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt **true** zurück, wenn der Vorgang erfolgreich war. Andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss. Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen Shell32.dll, um ein Modul Handle abzurufen. Dann rufe Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordinalzahl 259 auf, um diese Funktion zu verwenden.

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

 

 
