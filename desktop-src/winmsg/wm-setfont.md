---
description: Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959810"
---
# <a name="wm_setfont-message"></a>WM- \_ setFont-Nachricht

Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für die Schriftart (**hFont**). Wenn dieser Parameter **null** ist, verwendet das Steuerelement die Standardsystem Schriftart, um Text zu zeichnen.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort von *LPARAM* gibt an, ob das Steuerelement sofort nach dem Festlegen der Schriftart neu gezeichnet werden soll. Wenn dieser Parameter **true** ist, zeichnet sich das Steuerelement selbst neu auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **WM- \_ setFont** -Nachricht gilt für alle Steuerelemente, nicht nur für die in Dialogfeldern.

Die beste Zeit für das Festlegen der Schriftart des Steuer Elements durch den Besitzer eines Dialogfeld-Steuer Elements ist, wenn die " [**WM \_ InitDialog**](../dlgbox/wm-initdialog.md) "-Meldung empfangen wird. Die Anwendung sollte die [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) -Funktion aufrufen, um die Schriftart zu löschen, wenn Sie nicht mehr benötigt wird. Dies ist beispielsweise der Fall, wenn das Steuerelement zerstört wird.

Die Größe des Steuer Elements ändert sich nicht, wenn diese Nachricht empfangen wird. Um Clipping-Text zu vermeiden, der nicht in die Begrenzungen des Steuer Elements passt, sollte die Anwendung die Größe des Steuerelement Fensters korrigieren, bevor die Schriftart festgelegt wird.

Wenn ein Dialogfeld den [DS- \_ setFont](../dlgbox/about-dialog-boxes.md) -Stil verwendet, um den Text in seinen Steuerelementen festzulegen, sendet das System die **WM- \_ setFont** -Nachricht an die Dialogfeld Prozedur, bevor die Steuerelemente erstellt werden. Eine Anwendung kann ein Dialogfeld erstellen, das den DS-setFont-Stil enthält, indem Sie eine \_ der folgenden Funktionen aufruft:

-   [**"Kreatedialogindirect"**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**"Kreatedialogindirectparam"**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**Dialogboxindirekte**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**Dialogboxderedereparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**"Kreatedialogindirect"**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**"Kreatedialogindirectparam"**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**Dialogboxindirekte**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**Dialogboxderedereparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**Makelparam**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM- \_ getFont**](wm-getfont.md)
</dt> <dt>

[**WM \_ InitDialog**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
