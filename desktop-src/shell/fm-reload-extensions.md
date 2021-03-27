---
description: Wird von einer Datei-Manager-Erweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs erneut lädt, die im \[ Abschnitt "Addons" \] der Winfile.ini Datei aufgeführt sind.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: FM_RELOAD_EXTENSIONS Meldung (WF. h)
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
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979713"
---
# <a name="fm_reload_extensions-message"></a>FM-Nachricht zum erneuten \_ Laden \_

Wird von einer Datei-Manager-Erweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs erneut lädt, die im \[ Abschnitt "Addons" \] der Winfile.ini Datei aufgeführt sind.

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

## <a name="remarks"></a>Bemerkungen

Andere Anwendungen können die [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion verwenden, um diese Nachricht an den Datei-Manager zu senden. Zum Abrufen des entsprechenden Datei-Manager-Fenster Handles kann eine Anwendung \_ in einem Aufrufen der [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) -Funktion als *lpszClassName* -Parameter "WFS-Frame" angeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> </dl>

 

 
