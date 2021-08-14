---
description: Wird von einer Dateierweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs neu lädt, die im \[ Abschnitt AddOns \] der Winfile.ini-Datei aufgeführt sind.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: FM_RELOAD_EXTENSIONS-Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e4e632ac153a78e729ce0d3fcd65f49ae90781bd29cfe354d4571ba04e63be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224174"
---
# <a name="fm_reload_extensions-message"></a>\_FM RELOAD \_ EXTENSIONS-Meldung

Wird von einer Dateierweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs neu lädt, die im \[ Abschnitt AddOns \] der Winfile.ini-Datei aufgeführt sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Andere Anwendungen können die [**PostMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postmessagea) verwenden, um diese Nachricht an den Datei-Manager zu senden. Um das entsprechende Datei-Manager-Fensterhandle abzurufen, kann eine Anwendung "WFS \_ Frame" als *lpszClassName-Parameter* in einem Aufruf der [**FindWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-findwindowa) angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
