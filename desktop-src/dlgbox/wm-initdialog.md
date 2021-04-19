---
title: WM_INITDIALOG Meldung (Winuser. h)
description: Wird an die Dialogfeld Prozedur gesendet, unmittelbar bevor ein Dialogfeld angezeigt wird. Dialog Feld Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungs Aufgaben auszuführen, die sich auf die Darstellung des Dialog Felds auswirken.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Dialog Felder WM_INITDIALOG Meldung
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346737"
---
# <a name="wm_initdialog-message"></a>WM- \_ InitDialog-Meldung

Wird an die Dialogfeld Prozedur gesendet, unmittelbar bevor ein Dialogfeld angezeigt wird. Dialog Feld Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungs Aufgaben auszuführen, die sich auf die Darstellung des Dialog Felds auswirken.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das-Steuerelement, das den Standardtastatur Fokus erhalten soll. Das System weist den Standardtastatur Fokus nur zu, wenn die Dialogfeld Prozedur **true** zurückgibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zusätzliche Initialisierungs Daten. Diese Daten werden als lParam-Parameter in einem aufgerufen, der zum Erstellen des Dialog Felds verwendet wird [](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) , als *LPARAM* - [](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)Parameter in einem aufzurufenden [](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)Befehl [**an die Funktion**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)"" von "". Bei Eigenschaften Blättern ist dieser Parameter ein Zeiger auf die [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur, die zum Erstellen der Seite verwendet wird. Dieser Parameter ist 0 (null), wenn eine andere Dialogfeld-Erstellungs Funktion verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Dialogfeld Prozedur sollte **true** zurückgeben, um das System anzuweisen, den Tastaturfokus auf das von *wParam* angegebene Steuerelement festzulegen. Andernfalls sollte **false** zurückgegeben werden, um zu verhindern, dass das System den Standardtastatur Fokus festlegt.

Die Dialogfeld Prozedur sollte den Wert direkt zurückgeben. Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Das Steuerelement, das den Standardtastatur Fokus erhält, ist immer das erste Steuerelement im Dialogfeld, das sichtbar und nicht deaktiviert ist und das die **WS \_ Tabstopps** -Format aufweist. Wenn die Dialogfeld Prozedur **true** zurückgibt, prüft das System das Steuerelement, um sicherzustellen, dass es von der Prozedur nicht deaktiviert wurde. Wenn Sie deaktiviert wurde, legt das System den Tastaturfokus auf das nächste Steuerelement fest, das sichtbar und nicht deaktiviert ist und über das **WS \_ Tabstopps** verfügt.

Eine Anwendung kann nur dann **false** zurückgeben, wenn Sie den Tastaturfokus auf eines der Steuerelemente des Dialog Felds festgelegt hat.

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

[**"Kreatedialogindirectparam"**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**"Kreatedialogparam"**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**Dialogboxderedereparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

