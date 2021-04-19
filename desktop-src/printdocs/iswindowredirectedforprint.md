---
description: Die iswindowredirectedforprint-Funktion bestimmt, ob das angegebene Fenster zurzeit zum Drucken umgeleitet wird.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Iswindowredirectedforprint-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362965"
---
# <a name="iswindowredirectedforprint-function"></a>Iswindowredirectedforprint-Funktion

Die **iswindowredirectedforprint** -Funktion bestimmt, ob das angegebene Fenster zurzeit zum Drucken umgeleitet wird.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Das Handle des Fensters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Fenster zurzeit zum Drucken umgeleitet wird, gibt die Funktion einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein Fenster wird zum Drucken umgeleitet, wenn ein Aufrufen von [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)verarbeitet wird. In einem Aufrufen von **PrintWindow** rendert ein Fenster seinen Inhalt auf einem Offscreen-Gerätekontext.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**WM- \_ Druck**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM- \_ printclient**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

