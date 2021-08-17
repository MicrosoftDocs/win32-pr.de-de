---
title: WM_CTLCOLORBTN (Winuser.h)
description: Die WM CTLCOLORBTN-Nachricht wird an das übergeordnete Fenster einer Schaltfläche gesendet, \_ bevor die Schaltfläche gezeichnunget wird. Das übergeordnete Fenster kann den Text und die Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Meldung verarbeitet.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5689d7c76499f1ed180f76831af325c5e311bf06e052ea1446805c39ddf8642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407639"
---
# <a name="wm_ctlcolorbtn-message"></a>WM \_ CTLCOLORBTN-Meldung

Die **WM \_ CTLCOLORBTN-Nachricht** wird an das übergeordnete Fenster einer Schaltfläche gesendet, bevor die Schaltfläche gezeichnunget wird. Das übergeordnete Fenster kann den Text und die Hintergrundfarben der Schaltfläche ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das diese Meldung verarbeitet.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **HDC,** das das Handle für den Anzeigekontext für die Schaltfläche angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **HWND,** das das Handle für die Schaltfläche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss sie ein Handle an einen Pinsel zurückgeben. Das System verwendet den Pinsel, um den Hintergrund der Schaltfläche zu zeichnen.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung einen von ihr erstellten Pinsel zurückgibt (z. B. mithilfe der [**CreateSolidBrush-**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) oder [**CreateBrushIndirect-Funktion),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) muss die Anwendung den Pinsel frei geben. Wenn die Anwendung einen Systempinsel zurückgibt (z. B. einen, der von der [**GetStockObject-**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) oder [**GetSysColorBrush-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) abgerufen wurde), muss die Anwendung den Pinsel nicht freigibt.

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für die Schaltfläche aus. Schaltflächen mit den [**Formaten BS \_ PUSHBUTTON,**](button-styles.md) [**BS \_ DEFPUSHBUTTON**](button-styles.md)oder [**BS \_ PUSHLIKE**](button-styles.md) verwenden nicht den zurückgegebenen Pinsel. Schaltflächen mit diesen Stilen werden immer mit den Standardsystemfarben gezeichnet. Das Zeichnen von Pushschaltflächen erfordert mehrere unterschiedliche Pinsel: Gesicht, Hervorhebung und Schatten. Die **\_ WM-CTLCOLORBTN-Nachricht** lässt jedoch nur die Rückkehr eines Pinsels zu. Verwenden Sie eine vom Besitzer gezeichnete Schaltfläche, um eine benutzerdefinierte Darstellung für Schaltflächen zu ermöglichen. Weitere Informationen finden Sie unter [Creating Owner-Drawn Controls](user-controls-intro.md).

Die **WM \_ CTLCOLORBTN-Nachricht** wird nie zwischen Threads gesendet. Es wird nur innerhalb eines Threads gesendet.

Die Textfarbe eines Kontrollkästchens oder Optionsfelds gilt für das Kontrollkästchen oder die Schaltfläche, dessen Häkchen und den Text. Das Fokusrechteck für diese Schaltflächen bleibt die Standardfarbe des Systems (in der Regel Schwarz). Die Textfarbe eines Gruppenfelds gilt für den Text, aber nicht für die Zeile, die das Feld definiert. Die Textfarbe einer Schaltfläche gilt nur für das Fokusrechteck. Sie wirkt sich nicht auf die Farbe des Texts aus.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert **in eine INT \_ PTR-Datei** casten und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE zurückgibt,** wird die Standardnachrichtenbehandlung ausgeführt. Der von der \_ [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) MSGRESULT-DWL-Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**Wählen SiePalette aus.**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

