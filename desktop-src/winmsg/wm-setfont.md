---
description: Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199936"
---
# <a name="wm_setfont-message"></a>WM \_ SETFONT-Nachricht

Legt die Schriftart fest, die ein Steuerelement beim Zeichnen von Text verwenden soll.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für die Schriftart (**HFONT**). Wenn dieser Parameter **NULL** ist, verwendet das Steuerelement die Standardschriftart des Systems, um Text zu zeichnen.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort *lParam* in niedriger Reihenfolge gibt an, ob das Steuerelement beim Festlegen der Schriftart sofort neu gezeichnet werden soll. Wenn dieser Parameter **TRUE** ist, zeichnet sich das Steuerelement selbst neu.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **WM \_ SETFONT-Meldung** gilt für alle Steuerelemente, nicht nur für steuerelemente in Dialogfeldern.

Der beste Zeitpunkt für den Besitzer eines Dialogfeldsteuerelements zum Festlegen der Schriftart des Steuerelements ist, wenn er die [**WM \_ INITDIALOG-Nachricht**](../dlgbox/wm-initdialog.md) empfängt. Die Anwendung sollte die [**DeleteObject-Funktion**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) aufrufen, um die Schriftart zu löschen, wenn sie nicht mehr benötigt wird. beispielsweise, nachdem es das Steuerelement zerstört hat.

Die Größe des Steuerelements ändert sich aufgrund des Empfangs dieser Nachricht nicht. Um Clippingtext zu vermeiden, der nicht in die Grenzen des Steuerelements passt, sollte die Anwendung die Größe des Steuerelementfensters korrigieren, bevor sie die Schriftart festlegt.

Wenn ein Dialogfeld den [DS \_ SETFONT-Stil](../dlgbox/about-dialog-boxes.md) verwendet, um den Text in seinen Steuerelementen festzulegen, sendet das System die **WM \_ SETFONT-Meldung** an die Dialogfeldprozedur, bevor die Steuerelemente erstellt werden. Eine Anwendung kann ein Dialogfeld erstellen, das den DS \_ SETFONT-Stil enthält, indem eine der folgenden Funktionen aufgerufen wird:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
