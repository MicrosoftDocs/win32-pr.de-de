---
description: Gibt an, dass der Benutzer die F1-Taste gedrückt hat.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: WM_HELP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979464"
---
# <a name="wm_help-message"></a>WM- \_ Hilfe Meldung

Gibt an, dass der Benutzer die F1-Taste gedrückt hat. Wenn ein Menü aktiv ist, wenn F1 gedrückt wird, wird die **WM- \_ Hilfe** an das Fenster gesendet, das dem Menü zugeordnet ist. andernfalls wird die **WM- \_ Hilfe** an das Fenster mit dem Tastaturfokus gesendet. Wenn kein Fenster den Tastaturfokus besitzt, wird die **WM- \_ Hilfe** an das derzeit aktive Fenster gesendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lphi* 
</dt> <dd>

Die Adresse einer [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die Informationen über das Menü Element, das Steuerelement, das Dialogfeld oder das Fenster enthält, für das die Hilfe angefordert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt die **WM- \_ Hilfe** an das übergeordnete Fenster eines untergeordneten Fensters oder an den Besitzer eines Fensters der obersten Ebene.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 
