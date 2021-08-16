---
description: Wird gesendet, wenn größe und position des Clientbereichs eines Fensters berechnet werden müssen. Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Inhalt des Clientbereichs des Fensters steuern, wenn sich die Größe oder Position des Fensters ändert.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: WM_NCCALCSIZE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a73b469a920bcba79cc19670a7b9536c1bac9e0b0ffcab7ddf5930b984dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200076"
---
# <a name="wm_nccalcsize-message"></a>WM \_ NCCALCSIZE-Meldung

Wird gesendet, wenn größe und position des Clientbereichs eines Fensters berechnet werden müssen. Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Inhalt des Clientbereichs des Fensters steuern, wenn sich die Größe oder Position des Fensters ändert.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn *wParam* **TRUE ist,** wird angegeben, dass die Anwendung angeben soll, welcher Teil des Clientbereichs gültige Informationen enthält. Das System kopiert die gültigen Informationen in den angegebenen Bereich innerhalb des neuen Clientbereichs.

Wenn *wParam* **FALSE ist,** muss die Anwendung nicht den gültigen Teil des Clientbereichs angeben.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn *wParam* **TRUE ist,** verweist *lParam* auf eine [**NCCALCSIZE-PARAMS-Struktur, \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) die Informationen enthält, die eine Anwendung verwenden kann, um die neue Größe und Position des Clientrechtecks zu berechnen.

Wenn *wParam* **FALSE ist,** *zeigt lParam* auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Beim Eintrag enthält die -Struktur das vorgeschlagene Fensterrechteck für das Fenster. Beim Beenden sollte die -Struktur die Bildschirmkoordinaten des entsprechenden Fensterclientbereichs enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn der *wParam-Parameter* **FALSE ist,** sollte die Anwendung 0 (null) zurückgeben.

Wenn *wParam* **TRUE ist,** sollte die Anwendung 0 (null) oder eine Kombination der folgenden Werte zurückgeben.

Wenn *wParam* **TRUE ist** und eine Anwendung 0 (null) zurückgibt, wird der alte Clientbereich beibehalten und an der oberen linken Ecke des neuen Clientbereichs ausgerichtet.



| Rückgabecode/-wert                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ ALIGNTOP-0x0010**</dt> <dt></dt> </dl>    | Gibt an, dass der Clientbereich des Fensters beibehalten und am oberen Ende der neuen Position des Fensters ausgerichtet werden soll. Um beispielsweise den Clientbereich an der oberen linken Ecke auszurichten, geben Sie die \_ WVR-Werte ALIGNTOP und **WVR \_ ALIGNLEFT** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Gibt an, dass der Clientbereich des Fensters beibehalten und an der rechten Seite der neuen Position des Fensters ausgerichtet werden soll. Um beispielsweise den Clientbereich an der unteren rechten Ecke auszurichten, geben Sie die **\_ WVR-Werte ALIGNRIGHT** und WVR \_ ALIGNBOTTOM zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ ALIGNLEFT-0x0020**</dt> <dt></dt> </dl>   | Gibt an, dass der Clientbereich des Fensters beibehalten und an der linken Seite der neuen Position des Fensters ausgerichtet werden soll. Um beispielsweise den Clientbereich an der unteren linken Ecke auszurichten, geben Sie die **\_ WVR-Werte ALIGNLEFT** und **WVR \_ ALIGNBOTTOM** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ ALIGNBOTTOM-0x0040**</dt> <dt></dt> </dl> | Gibt an, dass der Clientbereich des Fensters beibehalten und am unteren Rand der neuen Position des Fensters ausgerichtet werden soll. Um beispielsweise den Clientbereich an der oberen linken Ecke auszurichten, geben Sie die \_ WVR-Werte ALIGNTOP und **WVR \_ ALIGNLEFT** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW-0x0100**</dt> <dt></dt> </dl>     | Wird in Kombination mit anderen Werten außer **WVR \_ VALIDRECTS** verwendet, wird das Fenster vollständig neu gezeichnet, wenn sich die Größe des Clientrechtecks horizontal ändert. Dieser Wert ähnelt dem [CS \_ HREDRAW-Klassenstil.](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ VREDRAW**</dt> <dt>0x0200</dt> </dl>     | Wird in Kombination mit anderen Werten außer **WVR \_ VALIDRECTS** verwendet, wird das Fenster vollständig neu gezeichnet, wenn sich die Größe des Clientrechtecks vertikal ändert. Dieser Wert ähnelt dem [CS \_ VREDRAW-Klassenstil.](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ REDRAW-0x0300**</dt> <dt></dt> </dl>      | Dieser Wert bewirkt, dass das gesamte Fenster neu gezeichnet wird. Es handelt sich um eine Kombination aus **WVR \_ HREDRAW-** und **WVR \_ VREDRAW-Werten.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | Dieser Wert gibt an, dass bei rückgabe von [**WM \_ NCCALCSIZE**](wm-nccalcsize.md)die rechtecke, die von **den rgrc** \[ 1- und \] **rgrc** 2-Membern der \[ \] [**NCCALCSIZE \_ PARAMS-Struktur**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) angegeben werden, gültige Ziel- bzw. Quellbereichrechtecke enthalten. Das System kombiniert diese Rechtecke, um den Bereich des zu erhaltenden Fensters zu berechnen. Das System kopiert alle Teile des Fensterbilds, die sich innerhalb des Quellrechtecks befinden, und schneidest das Bild in das Zielrechteck. Beide Rechtecke befinden sich in übergeordneten oder bildschirm relativen Koordinaten. Dieses Flag kann nicht mit anderen Flags kombiniert werden. <br/> Mit diesem Rückgabewert kann eine Anwendung aufwendigere Strategien zur Beibehaltung des Clientbereichs implementieren, z. B. das Zentrieren oder Beibehalten einer Teilmenge des Clientbereichs.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Fenster kann neu gezeichnet werden, je nachdem, ob der [CS \_ HREDRAW-](about-window-classes.md) oder CS \_ VREDRAW-Klassenstil angegeben ist. Dies ist die abwärtskompatible Standardverarbeitung dieser Nachricht durch die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (zusätzlich zur üblichen Clientrechteckberechnung, die in der obigen Tabelle beschrieben wird).

Wenn *wParam* **TRUE** ist, wird die Größe des Clientbereichs auf die Größe des Fensters einschließlich des Fensterrahmens geändert, wenn einfach 0 (0) ohne Verarbeitung der [**NCCALCSIZE-PARAMS-Rechtecke \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) zurückgibt. Dadurch werden der Fensterrahmen und die Beschriftungselemente aus dem Fenster entfernt, und nur der Clientbereich wird angezeigt.

Ab Windows Vista wirkt sich das Entfernen des Standardframes durch einfache Rückgabe von "0", wenn *wParam* **TRUE** ist, nicht auf Frames aus, die mithilfe der [**DwmExtendFrameIntoClientArea-Funktion**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) in den Clientbereich erweitert werden. Nur der Standardframe wird entfernt.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**NCCALCSIZE-PARAMETER \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
