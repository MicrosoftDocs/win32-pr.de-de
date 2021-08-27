---
title: WM_INITDIALOG (Winuser.h)
description: Wird unmittelbar vor dem Anzeigen eines Dialogfelds an die Dialogfeldprozedur gesendet. Dialogfeld-Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungsaufgaben auszuführen, die sich auf die Darstellung des Dialogfelds auswirken.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG meldungsdialogfelder
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
ms.openlocfilehash: e272ac93514fb60069a9217c3100318f95b1e9a8c77d9e75af56e2e7fbfbf66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117770"
---
# <a name="wm_initdialog-message"></a>WM \_ INITDIALOG-Meldung

Wird unmittelbar vor dem Anzeigen eines Dialogfelds an die Dialogfeldprozedur gesendet. Dialogfeld-Prozeduren verwenden diese Meldung in der Regel, um Steuerelemente zu initialisieren und alle anderen Initialisierungsaufgaben auszuführen, die sich auf die Darstellung des Dialogfelds auswirken.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Steuerelement, um den Standardtastaturfokus zu erhalten. Das System weist den Standardtastaturfokus nur zu, wenn die Dialogfeldprozedur **TRUE zurückgibt.**

</dd> <dt>

*lParam* 
</dt> <dd>

Zusätzliche Initialisierungsdaten. Diese Daten werden in einem Aufruf der Funktion [**CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) [**CreateDialogParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)oder [**DialogBoxParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) die zum Erstellen des Dialogfelds verwendet wird, als *lParam-Parameter* an das System übergeben. Bei Eigenschaftenblättern ist dieser Parameter ein Zeiger auf die [**PROPSHEETPAGE-Struktur,**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) die zum Erstellen der Seite verwendet wird. Dieser Parameter ist 0 (null), wenn eine andere Funktion zum Erstellen eines Dialogfelds verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Dialogfeldprozedur sollte **TRUE zurückgeben,** damit das System den Tastaturfokus auf das von *wParam* angegebene Steuerelement festlegen kann. Andernfalls sollte FALSE zurückgegeben **werden,** um zu verhindern, dass das System den Standardtastaturfokus festlegen kann.

Die Dialogfeldprozedur sollte den Wert direkt zurückgeben. Der von der [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) **\_ MSGRESULT-DWL-Wert** wird ignoriert.

## <a name="remarks"></a>Hinweise

Das Steuerelement, das den Standardtastaturfokus erhalten soll, ist immer das erste Steuerelement im Dialogfeld, das sichtbar und nicht deaktiviert ist und über das **WS \_ TABSTOP-Format** verfügt. Wenn die Dialogfeldprozedur **TRUE zurückgibt,** überprüft das System das Steuerelement, um sicherzustellen, dass es von der Prozedur nicht deaktiviert wurde. Wenn sie deaktiviert wurde, legt das System den Tastaturfokus auf das nächste Steuerelement fest, das sichtbar und nicht deaktiviert ist und **über das WS \_ TABSTOP verfügt.**

Eine Anwendung kann **NUR FALSE** zurückgeben, wenn sie den Tastaturfokus auf eines der Steuerelemente des Dialogfelds festgelegt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

