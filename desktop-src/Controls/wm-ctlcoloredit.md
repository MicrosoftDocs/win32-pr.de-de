---
title: WM_CTLCOLOREDIT (Winuser.h)
description: Ein Bearbeitungssteuer steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die WM CTLCOLOREDIT-Nachricht an das übergeordnete Fenster, wenn das Steuerelement \_ gezeichnet werden soll.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7f1fd27c51cabc699cf945fd4701c36d2e9709d1654de45859777333b9b4bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053900"
---
# <a name="wm_ctlcoloredit-message"></a>WM \_ CTLCOLOREDIT-Meldung

Ein Bearbeitungssteuer steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die **WM \_ CTLCOLOREDIT-Nachricht** an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll. Wenn auf diese Meldung reagiert wird, kann das übergeordnete Fenster das angegebene Gerätekontexthand handle verwenden, um den Text und die Hintergrundfarben des Bearbeitungssteuerfelds festzulegen.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für das Bearbeitungssteuerungsfenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungssteuer steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss sie das Handle eines Pinsels zurückgeben. Das System verwendet den Pinsel, um den Hintergrund des Bearbeitungssteuer steuerelements zu zeichnen.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung einen von ihr erstellten Pinsel zurückgibt (z. B. mithilfe der [**CreateSolidBrush-**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) oder [**CreateBrushIndirect-Funktion),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) muss die Anwendung den Pinsel frei geben. Wenn die Anwendung einen Systempinsel zurückgibt (z. B. einen, der von der [**GetStockObject-**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) oder [**GetSysColorBrush-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) abgerufen wurde), muss die Anwendung den Pinsel nicht freigibt.

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für das Bearbeitungssteuerprogramm aus.

Schreibgeschützte oder deaktivierte Bearbeitungssteuerelemente senden die **\_ WM-CTLCOLOREDIT-Nachricht** nicht. Stattdessen senden sie die [**\_ WM-CTLCOLORSTATIC-Nachricht.**](wm-ctlcolorstatic.md)

Die **WM \_ CTLCOLOREDIT-Nachricht** wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert **in eine INT \_ PTR-Datei** casten und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE zurückgibt,** wird die Standardnachrichtenbehandlung ausgeführt. Der von der \_ [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) MSGRESULT-DWL-Wert wird ignoriert.

**Umfangreiche Bearbeitung:** Diese Meldung wird nicht unterstützt. Verwenden Sie die MELDUNG [**EM \_ SETBKGNDCOLOR,**](em-setbkgndcolor.md) um die Hintergrundfarbe für ein umfangreiches Bearbeitungssteuer steuerelement fest zu legen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**Wählen SiePalette aus.**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

