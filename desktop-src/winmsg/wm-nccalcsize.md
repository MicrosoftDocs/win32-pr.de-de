---
description: Wird gesendet, wenn die Größe und die Position des Client Bereichs eines Fensters berechnet werden müssen. Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Inhalt des Client Bereichs des Fensters steuern, wenn sich die Größe oder Position des Fensters ändert.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: WM_NCCALCSIZE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362487"
---
# <a name="wm_nccalcsize-message"></a>WM \_ nccalcsize-Nachricht

Wird gesendet, wenn die Größe und die Position des Client Bereichs eines Fensters berechnet werden müssen. Durch die Verarbeitung dieser Nachricht kann eine Anwendung den Inhalt des Client Bereichs des Fensters steuern, wenn sich die Größe oder Position des Fensters ändert.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn *wParam* auf **true** festgelegt ist, gibt es an, dass die Anwendung angeben soll, welcher Teil des Client Bereichs gültige Informationen enthält. Das System kopiert die gültigen Informationen in den angegebenen Bereich innerhalb des neuen Client Bereichs.

Wenn *wParam* den Wert **false** hat, muss die Anwendung den gültigen Teil des Client Bereichs nicht angeben.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn *wParam* auf **true** festgelegt ist, verweist *LPARAM* auf eine [**nccalcsize- \_ params**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) -Struktur, die Informationen enthält, die eine Anwendung verwenden kann, um die neue Größe und Position des Client Rechtecks zu berechnen.

Wenn *wParam* den Wert **false** hat, verweist *LPARAM* auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Beim-Eintrag enthält die-Struktur das vorgeschlagene Fenster Rechteck für das Fenster. Beim Beenden sollte die-Struktur die Bildschirm Koordinaten des entsprechenden Fenster Client Bereichs enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn der *wParam* -Parameter **false** ist, muss die Anwendung 0 (null) zurückgeben.

Wenn *wParam* den Wert **true** hat, sollte die Anwendung 0 (null) oder eine Kombination der folgenden Werte zurückgeben.

Wenn *wParam* den Wert **true** hat und eine Anwendung 0 (null) zurückgibt, wird der alte Client Bereich beibehalten und an der oberen linken Ecke des neuen Client Bereichs ausgerichtet.



| Rückgabecode/-wert                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ AlignTop**</dt> <dt>0x0010</dt> </dl>    | Gibt an, dass der Client Bereich des Fensters beibehalten und am oberen Rand der neuen Position des Fensters ausgerichtet werden soll. Wenn Sie z. b. den Client Bereich in der oberen linken Ecke ausrichten möchten, geben Sie die Werte WVR \_ AlignTop und **WVR \_ alignleft** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ AlignRight**</dt> <dt>0x0080</dt> </dl>  | Gibt an, dass der Client Bereich des Fensters beibehalten und an der rechten Seite der neuen Position des Fensters ausgerichtet werden soll. Wenn Sie z. b. den Client Bereich in der unteren rechten Ecke ausrichten möchten, geben Sie die Werte **WVR \_ AlignRight** und WVR \_ AlignBottom zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ Alignleft**</dt> <dt>0x0020</dt> </dl>   | Gibt an, dass der Client Bereich des Fensters beibehalten und an der linken Seite der neuen Position des Fensters ausgerichtet werden soll. Wenn Sie den Client Bereich z. b. an der unteren linken Ecke ausrichten möchten, geben Sie die Werte **WVR \_ alignleft** und **WVR \_ AlignBottom** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ AlignBottom**</dt> <dt>0x0040</dt> </dl> | Gibt an, dass der Client Bereich des Fensters beibehalten und am unteren Rand der neuen Position des Fensters ausgerichtet werden soll. Wenn Sie z. b. den Client Bereich an der linken oberen Ecke ausrichten möchten, geben Sie die Werte WVR \_ AlignTop und **WVR \_ alignleft** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ Hredraw**</dt> <dt>0x0100</dt> </dl>     | Wird in Kombination mit anderen Werten mit Ausnahme von **WVR \_ validrects** verwendet und bewirkt, dass das Fenster vollständig neu gezeichnet wird, wenn die Größe des Client Rechtecks horizontal geändert wird. Dieser Wert ähnelt dem [CS \_ hredraw](about-window-classes.md) -Klassen Stil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ Vredraw**</dt> <dt>0x0200</dt> </dl>     | Wird in Kombination mit anderen Werten mit Ausnahme von **WVR \_ validrects** verwendet und bewirkt, dass das Fenster vollständig neu gezeichnet wird, wenn sich die Größe des Client Rechtecks vertikal ändert. Dieser Wert ähnelt dem [CS \_ vredraw](about-window-classes.md) -Klassen Stil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_**</dt> <dt>0x0300</dt> neu zeichnen </dl>      | Dieser Wert bewirkt, dass das gesamte Fenster neu gezeichnet wird. Es handelt sich um eine Kombination aus **WVR- \_ hredraw** -und **WVR- \_ vredraw** -Werten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ Validrects**</dt> <dt>0x0400</dt> </dl>  | Dieser Wert gibt an, dass bei Rückgabe von [**WM \_ nccalcsize**](wm-nccalcsize.md)die Rechtecke, die von den Elementen **rgrc** \[ 1 \] und **rgrc** \[ 2 \] der [**nccalcsize \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) -Parameter Struktur angegeben werden, gültige Ziel-und Quell Bereichs Rechtecke enthalten. Das System kombiniert diese Rechtecke, um den Bereich des Fensters zu berechnen, der beibehalten werden soll. Das System kopiert jeden Teil des Fenster Bilds, der sich innerhalb des Quell Rechtecks befindet, und schneidet das Bild an das Ziel Rechteck. Beide Rechtecke befinden sich in Bezug auf über-und relative oder Bildschirm relative Koordinaten. Dieses Flag kann nicht mit anderen Flags kombiniert werden. <br/> Mit diesem Rückgabewert kann eine Anwendung ausführlichere Client Bereichs Erhaltungsstrategien implementieren, z. b. das zentrieren oder beibehalten einer Teilmenge des Client Bereichs.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Fenster wird ggf. neu gezeichnet, je nachdem, ob der Klassen Stil [CS \_ hredraw](about-window-classes.md) oder CS \_ vredraw angegeben ist. Dies ist die standardmäßige abwärts kompatible Verarbeitung dieser Nachricht durch die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion (zusätzlich zur üblichen Berechnung des Client Rechtecks, die in der obigen Tabelle beschrieben wird).

Wenn *wParam* den Wert **true** hat, wird die Größe des Client Bereichs in der Größe des Fensters, einschließlich des Fensterrahmens, ohne die Verarbeitung der [**nccalcsize \_ -**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) Rechtecke auf "0" zurückgegeben. Hierdurch werden der Fensterrahmen und die Beschriftungs Elemente aus dem Fenster entfernt, sodass nur der Client Bereich angezeigt wird.

Ab Windows Vista wirkt sich das Entfernen des Standardrahmens durch einfaches zurückgeben von 0, wenn der *wParam* -Wert **true** ist, nicht auf Frames aus, die mithilfe der Funktion [**dwmextendframeinesclientarea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) in den Client Bereich erweitert werden. Nur der Standardrahmen wird entfernt.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Fenster**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**nccalcsize \_ -Parameter**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
