---
description: Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü oder Symbolleisten-Befehls Element drückt. Die Erweiterung sollte WinHelp aufrufen, wobei der hWnd-Parameter der Funktion auf den Wert des HWND-Parameters der Erweiterung festgelegt ist.
title: FMEVENT_HELPMENUITEM Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977089"
---
# <a name="fmevent_helpmenuitem-message"></a>Meldung zu "f mevent \_ helpmenuitem"

Wird an eine DLL-Prozedur der Datei-Manager-Erweiterung gesendet, wenn der Benutzer F1 in einem Menü oder Symbolleisten-Befehls Element drückt. Die Erweiterung sollte [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufrufen, wobei der *HWND* -Parameter der Funktion auf den Wert des *HWND* -Parameters der Erweiterung festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*uitem* 
</dt> <dd>

Ein-Wert, der das Menü oder das Symbolleisten-Befehls Element identifiziert, für das die Hilfe gewünscht ist. Die Erweiterungs Prozedur verwendet diesen Wert, um zu bestimmen, wie [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)am besten aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL-Prozedur sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> <dt>

[**-HelpString für "f" \_**](fmevent-helpstring.md)
</dt> </dl>

 

 




